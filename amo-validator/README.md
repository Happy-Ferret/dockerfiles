# Pre-requisites:

Install [docker](http://docs.docker.com/) 

# How to use it:

## Using my image from https://hub.docker.com/

    docker run --rm -v <path-to-dir-of-xpi>:/xpi marceloandrader/amo-validator /xpi/file.xpi -t extension 


## Using the image by building it yourself:

    docker build -t=<yourname>/amo-validator .
    docker run --rm -v <path-to-dir-of-xpi>:/xpi <yourname>/amo-validator /xpi/file.xpi -t extension 

