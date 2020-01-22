FROM node:latest
MAINTAINER Thiago Orbite
COPY . /var/www
WORKDIR /var/www
RUN npm install
ENTRYPOINT npm start
EXPOSE 3000
#deletado a pasta "node_modules"