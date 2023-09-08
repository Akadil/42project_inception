# Use debian as a base image
FROM debian:buster

# Install basic dependencies
RUN apt-get update -y
RUN apt-get install -y nginx
RUN apt-get install -y vim
RUN apt-get install -y curl
RUN mkdir -p /etc/nginx/ssl

RUN openssl req -x509 -nodes -out /etc/nginx/ssl/inception.crt -keyout /etc/nginx/ssl/inception.key -subj "/c=FR/ST=IDF/L=Paris/O=42/OU=42/CN=akalimol.42.fr/UID=akalimol"

RUN mkdir -p /var/run/nginx
COPY ./conf/nginx.conf /etc/nginx/nginx.conf
