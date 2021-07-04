# :memo: Notes
## Docker

### Resources
* [:copyright: Docker](https://www.docker.com/)
* [:copyright: Docker Hub](https://hub.docker.com/)
* [:copyright: Docker Docs](https://docs.docker.com/)

### Terms and concepts
* Docker Hub Service (Repositories for storing and sharing images)
* Image (Similar to template, class)
* Container (Similar to instance, object.  It must contain everything needed to run an application)
  - Operative System
  - Dependencies
  - Configuration
  - Scripts
  - Binaries
  - Application
  - etc

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
Setup container image
```
$ vi Dockerfile
```
Dockerfile
```
FROM <repo_name>:<version> (e.g. alpine, slim-buster)
```
Build container image
```
$ docker build  -t <name> .
```
View images
```
$ docker images
```
Delete image
```
$ docker image rm <id>
```
Run the application
```
$ docker run -it <id_image>
$ docker run -it -p 80:80 <id_image>
```
Stop container
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
Delete everything - Remove all unused containers, volumes, networks and images
```
$ docker system prune -a --volumes
```
#### Create a new container image
Setup container image
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
Build container image
```
$ docker build  -t <name> .
```
Run the application
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
