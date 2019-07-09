FROM ubuntu:18.04
RUN apt-get update
RUN apt-get install -y nginx inetutils-ping
CMD ["ping", "-c", "3", "8.8.8.8"]
