FROM ubuntu:14.04
MAINTAINER Marcelo Andrade <marcelo.andrade.r@gmail.com>

RUN apt-get update -y
RUN apt-get install -y python
RUN apt-get install -y autoconf2.13
RUN apt-get install -y curl
RUN apt-get install -y unzip
RUN apt-get install -y git
RUN apt-get install -y python-dev
RUN apt-get install -y python-pip

RUN mkdir /amo-validator
WORKDIR /amo-validator

# Install spidermonkey
RUN curl http://ftp.mozilla.org/pub/mozilla.org/firefox/nightly/latest-trunk/jsshell-linux-x86_64.zip -o jsshell-linux-x86_64.zip
RUN unzip jsshell-linux-x86_64.zip
RUN rm  jsshell-linux-x86_64.zip
ENV SPIDERMONKEY_INSTALLATION /amo-validator

# Clone amo-validator
RUN git clone --recursive git://github.com/mozilla/amo-validator.git
WORKDIR /amo-validator/amo-validator
RUN pip install -r requirements.txt

ENTRYPOINT ["/usr/bin/sudo", "./addon-validator"]
CMD ["-h"]
