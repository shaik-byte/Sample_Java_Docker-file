
#### Steps

##### Clone source code from git
```
$  git clone https://github.com/dstar55/docker-hello-world-spring-boot .
```

##### Build Docker image
```
$ docker build -t="hello-world-java" .
```
Maven build will be executes during creation of the docker image.

>Note:if you run this command for first time it will take some time in order to download base image from [DockerHub](https://hub.docker.com/)

##### Run Docker Container
```
$ docker run -p 8080:8080 -it --rm hello-world-java
```

##### Test application

```
$ curl localhost:8080
```

the respone should be:
```
Hello World
```

#####  Stop Docker Container:
```
docker stop `docker container ls | grep "hello-world-java:*" | awk '{ print $1 }'`
```

## Run with docker-compose 

Build and start the container by running 

```
$ docker-compose up -d 
```

##### Test application with ***curl*** command

```
$ curl localhost:8080
```

the respone should be:
```
Hello World
```

##### Stop Docker Container:
```
docker-compose down
```
