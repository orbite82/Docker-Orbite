FROM debian 

MAINTAINER Thiago Orbite <thiagoorbite@gmail.com>

LABEL app="Orbitex"
ENV ORBITE="Dockerfile-Orbite"

RUN apt-get update && apt-get install -y stress && apt-get clean

CMD stress --cpu 1 --vm-bytes 64 --vm 1
