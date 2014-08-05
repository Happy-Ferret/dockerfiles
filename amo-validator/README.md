# How to build the image:

    docker build -t=<yourname>/amo-validator .


# How to use it, using my image on https://hub.docker.com/


    docker run --rm -v <path-to-dir-of-xpi>:/xpi marceloandrader/amo-validator /xpi/file.xpi -t extension 

