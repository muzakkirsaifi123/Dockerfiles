FROM ubuntu:latest
MAINTAINER Muzakkir
RUN apt-get update && apt-get install -y nginx && service nginx stop
#ADD index.nginx-debian.html /usr/www/nginx/html/index.nginx-debian.html

COPY index.html /var/www/html/

EXPOSE 80
