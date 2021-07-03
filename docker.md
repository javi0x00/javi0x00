# :memo: Notes
## Docker

### Resources
* [:copyright: Docker](https://www.docker.com/)
* [:copyright: Docker Hub](https://hub.docker.com/)

### Terms and concepts
* Container
  - Operative System
  - Dependencies
  - Application
* Image
* dockerhub Service

### Commands
#### Commons
```
$ docker -v
$ docker pull
$ docker run
$ docker stop
$ docker images
$ docker ps
$ docker start
$ docker logs
$ docker axec
```
#### Basic
```
$ vi Dockerfile
```
Dockerfile
```
FROM <repo_name>:<version> (e.g. alpine, slim-buster)
```
Build image
```
$ docker build  -t <name> .
```
Build container
```
$ docker run -it <id_image>
$ docker run -it -p 80:80 <id_image>
```
Stop image
```
$ docker stop
```
View all containers
```
$ docker ps -a
```
Delete all inactive containers
```
$ docker system prune 
```
View images
```
$ docker images
```
#### Create a new container
Setup
```
$ vi Dockerfile
```
Dockerfile
```
FROM ...
WORKDIR ...
COPY . /usr/src/app
WORKDIR /usr/src/app
RUN <command>
CMD [...]
ENTRYPOINT <command>
```
Build image
```
$ docker build  -t <name> .
```
Run image
```
$ docker run <name>
$ docker run -p 3000:3000 <name>
$ docker run -dp 3000:3000 <name>
$ docker run -d -v <path> -p 3000:3000 <name>
```
Stop image
```
$ docker stop <id>
```
Re-Build image
```
$ docker build  -t <repo_name>:<version> .
```
#### Share image
```
$ docker login
$ docker tag <id> <new_name>
docker push <name>
```
#### Docker network
Create
```
$ docker network create <name> ...
```
Run
```
$ docker run -it --network create <name> ...
$ docker run -dp 3000:3000 ...
```
#### Docker compose
Setup
```
$ vi docker-compose.yaml
```
docker-compose.yaml
```
version: ...
services: ...
```
Run
````
$ docker-compose up -d
```
Stop
````
$ docker-compose down
```
- - -
## Software Developer
[Javier Andrés Garzón Patarroyo](https://www.javierandresgp.com)
