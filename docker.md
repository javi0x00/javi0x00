# :memo: Notes
## Docker

### Resources
* [:copyright: Docker Hub](https://hub.docker.com/)

### Terms and concepts
* Image
* Container
* dockerhub Service

### Commands
#### Commons
```
$ docker pull
$ docker run
$ docker stop
$ docker images
$ docker ps
$ docker start
$ docker logs
$ docker axec
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
COPY . .
RUN ...
CMD [...]
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
$ docker stop
```
Re-Build image
```
$ docker build  -t <name>:<version> .
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
