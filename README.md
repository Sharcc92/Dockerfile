# Dockerinstructions:

# Docker Basics
## Setup

## To build an image run
```
sudo docker build -t docker_name . --no-cache
```
To create a docker container run
```
sudo docker run -it -d --network=host --name docker_name docker_name:latest bash
```
through setting --network=host, docker is in the same network as your host and can therefore interact with roscore.

## Starting with a dockerfile [dockerfile]
```






[dockerfile](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/#run)
