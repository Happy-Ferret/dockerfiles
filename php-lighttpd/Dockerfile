from ubuntu:14.04
maintainer Marcelo Andrade <marcelo.andrade.r@gmail.com>

run apt-get -y update 
run DEBIAN_FRONTEND=noninteractive apt-get -y upgrade
run DEBIAN_FRONTEND=noninteractive apt-get install -y software-properties-common
run locale-gen en_US.UTF-8
env LANG en_US.UTF-8
run add-apt-repository ppa:ondrej/php5-5.6
run apt-get -y update 
run DEBIAN_FRONTEND=noninteractive apt-get install -y git php5-cli php5-fpm php5-mysql php5-curl php5-memcached php5-readline php5-gearman php5-oauth curl lighttpd supervisor openssh-server
run curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin && mv /usr/local/bin/composer.phar /usr/local/bin/composer
## supervisor configuration
add supervisord.conf /etc/supervisor/conf.d/supervisord.conf
## lighttpd configuration
add lighttpd.conf /etc/lighttpd/lighttpd.conf
run lighttpd-enable-mod fastcgi
add php5-fpm.conf /etc/lighttpd/conf-enabled/php5-fpm.conf

run useradd dev
run mkdir /home/dev && chown -R dev: /home/dev
env HOME /home/dev
workdir /home/dev

run mkdir -p /app
workdir /app

run mkdir /var/run/sshd

expose 80
expose 22

CMD ["/usr/bin/supervisord"]
