default: build

build:
	docker build -t=marceloandrader/php-lighttpd .

run:
	docker run -d --name php -p 8080:80 -p 22 -v `pwd`:/app marceloandrader/php-lighttpd

clear:
	docker stop php
	docker rm php

enter:
	sudo docker-enter php

logs:
	docker logs php

publish:
	docker push marceloandrader/php-lighttpd
