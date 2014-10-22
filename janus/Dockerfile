FROM debian:latest
MANTAINER Marcelo Andrade <marcelo.andrade.r@gmail.com>

RUN apt-get -y update
RUN apt-get -y install vim
RUN apt-get -y install git
RUN apt-get -y install curl
RUN apt-get -y install ruby
RUN apt-get -y install rake
RUN apt-get -y install ack
RUN apt-get -y install ctags

RUN curl -Lo- https://bit.ly/janus-bootstrap | bash

CMD ["vi"]
