FROM resin/armv7hf-debian:jessie
MAINTAINER Brice Copy <brice.copy@gmail.com>


RUN apt-get update 
RUN apt-get upgrade
RUN apt-get install curl
RUN curl https://processing.org/download/install-arm.sh | sh

VOLUME ["/usr/lib/arm-linux-gnueabihf"]

#RUN apt-get autoremove -y
#RUN rm -rf /var/lib/apt/lists/*
WORKDIR /app

#CMD [""]
