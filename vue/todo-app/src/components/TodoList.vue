<template>
  <div>
    <todo v-on:delete-todo="deleteTodo"
    v-on:marked-todo="completeTodo"
    v-for="todo in todos"
    :key="todo.id"
    v-bind:todo="todo"></todo>
  </div>
</template>

<script type = "text/javascript" >

import Todo from './Todo';

export default {
  props: ['todos'],
  components: {
    Todo,
  },
  methods: {
    deleteTodo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos.pop(todoIndex);
    },
    completeTodo(todo) {
      /* eslint no-console: ["error", { allow: ["warn", "error"] }] */
      this.todos[this.todos.indexOf(todo)].done = !this.todos[this.todos.indexOf(todo)].done;
    },
  },
};
</script>
