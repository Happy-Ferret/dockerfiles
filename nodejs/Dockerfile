FROM ubuntu
MAINTAINER Marcelo Andrade <marcelo.andrade.r@gmail.com>

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y wget

RUN wget -q http://nodejs.org/dist/v0.10.26/node-v0.10.26-linux-x64.tar.gz -O /tmp/node.tar.gz
RUN cd /usr/local && tar --strip-components=1 -x -z -f /tmp/node.tar.gz && rm /tmp/node.tar.gz
