# :memo: Notes
## DOCKER
- - -
### Resources
* [:copyright: Docker](https://www.docker.com/)
* [:copyright: Docker Hub](https://hub.docker.com/)
* [:copyright: Docker Docs](https://docs.docker.com/)
### Terms and concepts
* Docker Hub Service (Repositories for storing and sharing images)
* Image (Similar to template, class)
  - Files
  - File tree
  - Settings
  * Layers set (read-only)
    - id
    - files
* Container (Similar to instance, object.  It must contain everything needed to run an application)
  - Operative System
  - Dependencies
  - Configuration
  - Scripts
  - Binaries
  - Application
  - etc
  * States
    - Running
    - Stoped
* Network
* Volume
### Image
Basic commands
```
$ docker search <image>
$ docker pull <image>
$ docker images
$ docker rm image <image>
$ docker build <parameter> <name_image> <path_context>
```
### Container
Basic commands
```
$ docker run <parameter (optional)> <image> <command (optional)>
$ docker exec <parameter (optional)> <container> <command>
$ docker ps <parameter (optional)>
$ docker stop <container>
$ docker start <container>
$ docker rm <parameter (optional)> <container>
```
### Network
Basic commands
```
$ docker network ls
$ docker network create <name>
$ docker network rm <network>
$ docker run --network <network>
$ docker run --port <host_port:container_port>
$ docker run --p <host_port:container_port>
```
### Volume
Basic commands
```
$ docker volume ls
$ docker volume create <name>
```
### Common commands
Basic
```
$ docker -v
$ docker logs
```
Delete everything - Remove all unused containers, volumes, networks and images
```
$ docker system prune -a --volumes
```
#### Dockerfile
Basic Setup
```
$ vi Dockerfile
```
Dockerfile
```
FROM <tag_image>
RUN mkdir -p <absolute_path>
WORKDIR <absolute_path>
COPY <path_context (relative path)> <path_image (absolute or relative path)>
RUN <command>
EXPOSE <port>
CMD <default_command>
```
.dockerignore
```
<directories and/or name files>
```
#### Docker compose
Basic Setup
```
$ vi docker-compose.yaml
```
docker-compose.yaml
```
version: <docker compose version>
services:
  <container image name>
    <options>
  <container image name>
    <options>
  ...
networks:
  <options>
volumes:
  <options>
```
Basic commands
```
$ docker-compose --version
$ docker-compose build
$ docker-compose up <parameters (optionals)> <services (optionals)>
$ docker-compose stop <services (optionals)>
$ docker-compose down
$ docker-compose run <parameters (optionals)> <services> <command (optional)>
$ docker-compose logs <parameters (optionals)> <services (optionals)>
```
###### Examples
Share image
```
$ docker build -t <username/image_name> .
$ docker login
$ docker push <username/image_name>
```
or
```
$ docker tag <id> <new_name>
$ docker push <name>
```
Create network
```
$ docker network create <name> ...
```
Run
```
$ docker run -it --network create <name> ...
$ docker run -dp 3000:3000 ...
```
Setup container image with dockerfile
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
Run the application (when run container image, it create a new container, a new process)
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
Setup container image with dockerfile
```
$ vi Dockerfile
```
Dockerfile
```
FROM ...
WORKDIR ...
COPY . .
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
- - -
## Software Developer
[Javier Andrés Garzón Patarroyo](https://www.javierandresgp.com)
