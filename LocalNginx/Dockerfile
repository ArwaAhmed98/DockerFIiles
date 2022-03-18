FROM ubuntu:latest

USER root

WORKDIR app

RUN apt-get update -y
RUN apt install nginx -y
RUN echo "Hellow"
ADD html.tar.gz /root
COPY conf.conf .

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]


