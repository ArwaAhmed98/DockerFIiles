#Build Stage Start

#Specify a base image
FROM node:alpine as builder 

#Specify a working directory
WORKDIR '/app'

#Copy the dependencies file
COPY package*.json /app/


#Install dependencies
RUN npm install -g npm@8.5.4

#Copy remaining files
COPY . .

#Build the project for production
#RUN apt-get install -y git-core curl build-essential openssl libssl-dev \
 #&& git clone https://github.com/nodejs/node.git \
 #&& cd node \
 #&& ./configure \
 #&& make \
#RUN npm install
RUN npm run build 

#Run Stage Start
FROM nginx

#Copy production build files from builder phase to nginx
COPY --from=builder /app/build /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
#CMD ["npm" , "start"]

#RUN npm start
