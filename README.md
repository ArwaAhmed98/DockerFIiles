# DockerFIiles
ITI 9 Month program - Docker Labs

# Prerequisites 
Install docker on your local machine 
# Local Nginx 

In order to run get  your own image of local nginx based on ubuntu:latest image
run ` docker build -t nginxdemo:v1 . ` 
In order to Run a container from your own image run ` docker run -it --name nameofnginxcontainer nginxdemo:v1 ` 
# Dockerize your react App using multistage docker file

In order to run react app containerized with a base image of nginx image in multistage dockerfile 
run `  docker build -t myreactapp . ` 
In order to Run a container from your own image run ` docker run -it --name dockerreact -p 80:80  myreactapp ` 
