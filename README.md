### Ubuntu Java Dockerfile

This repository will contain all the Dockerfiles needed to build the cluster at Penn State Great Valley. All the images in this project are nased on a base image that has Ubuntu and Java installed. This image is not intended to be run independently but rather as a base for other images.

The Dockerfile in this folder is to create a base Java for Docker's automated build.

## Base Docker Image

    psugv-bigdata/ubuntu_java

### Installation

1. Install Docker.

2. Download the Dockerfile and build the image using: 

    docker build -t psugv-bigdata/ubuntu-java .


###Usage

    docker run -it --name psuubuntujava psugv-bigdata/ubuntu-java /bin/bash

###Restart container

    docker start psuubuntujava
    docker exec -it psuubuntujava /bin/bash
    docker stop psuubuntujava

### Test java instalation

    docker run -it --rm psuubuntujava java

### Run javac

    docker run -it --rm psuubuntujava javac
