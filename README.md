# Basic Docker Flask Demo
Nikola Cucakovic, December 2019

## Overview
The purpose of this project is to showcase a basic example of using [Docker](https://www.docker.com/) and [Flask](https://palletsprojects.com/p/flask/) together. This is purely for educational purposes as I find the best way to learn is by practically doing. I plan to enhance this in the future by integrating a container management tool such as [Kubernetes](https://kubernetes.io/) or [Docker Swarm](https://docs.docker.com/engine/swarm/).

## Basic Usage
Without Docker Compose:

```docker
docker build -t basic-docker-flask-demo:latest .
docker run -d -p 5000:5000 basic-docker-flask-demo
```

To verify the container is running:
```
docker ps
```

## Useful Docker Commands

Search for existing docker containers: [docker search](https://docs.docker.com/engine/reference/commandline/search/):
```docker
docker search [OPTIONS] <TERM e.g ubuntu>
```

Run a docker container: [docker run](https://docs.docker.com/engine/reference/run/)
```docker
docker run -it <image e.g ubuntu:latest>
```

Copy files from host to docker container: [docker cp](https://docs.docker.com/engine/reference/commandline/cp/)
```docker
docker cp <local file> <container name>:<container path>
```

List docker containers: [docker ps / docker container](https://docs.docker.com/engine/reference/commandline/ps/)
```docker
docker ps -a
```

Start a stopped docker container in bash/shell interactive mode: [docker start](https://docs.docker.com/engine/reference/commandline/start/)
```docker
docker start -ai <container_name>
```

Stop all containers: [docker container stop](https://docs.docker.com/engine/reference/commandline/stop/)
```docker
docker container stop $(docker container ls -aq)
```

Remove all containers: [docker container rm](https://docs.docker.com/engine/reference/commandline/container_rm/)
```docker
docker container rm $(docker container ls -aq)
```

List docker images: [docker images](https://docs.docker.com/engine/reference/commandline/images/)
```docker
docker images -a
```

Remove unused images: [docker image prune](https://docs.docker.com/engine/reference/commandline/image_prune/)
```docker
docker image prune -a
```
