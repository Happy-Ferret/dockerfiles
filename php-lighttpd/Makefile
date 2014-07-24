default: build

build:
	docker build -t=marceloandrader/php-lighttpd .

run: clear
	docker run -d --name php -p 8080:80 -p 22 -v `pwd`:/srv/app marceloandrader/php-lighttpd

clear:
	docker stop php
	docker rm php

enter:
	sudo docker-enter php

logs:
	docker logs php
