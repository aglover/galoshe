# Galoshe

Your Dockered Spring Boot example, baby.

For more details, see my blog article entitled [Docker Containers With Gradle in 4 Steps](http://thediscoblog.com/blog/2014/06/13/docker-containers-with-gradle-in-4-steps/).
 
## Running w/o Docker

```
$ ./gradlew bootRun
```

Go to localhost:8080 and you'll see a simple message. 

## Docker'ing it

You'll need to have the `docker` binary locally w/this particular [Gradle Docker plugin](https://github.com/Transmode/gradle-docker).

```
$ ./gradlew distDocker
```

This will create a Docker image called `aglover/galoshe` -- type `docker ps` after this command finishes and you'll see it.
 
```
docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             VIRTUAL SIZE
aglover/galoshe     latest              332e163221bc        3 minutes ago       1.042 GB
dockerfile/java     latest              f9793c257930        3 weeks ago         1.026 GB
```

Firing it up is as easy as:

```
$ docker run <image id>
```

Pretty easy, yeah?