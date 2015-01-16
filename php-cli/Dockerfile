FROM php:5.6
RUN apt-get update -y
RUN apt-get install -y libmcrypt-dev
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install mcrypt
RUN docker-php-ext-install pdo_mysql
WORKDIR /app
