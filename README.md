# Galoshe

Your Dockered Spring Boot example, baby.
 
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

This will create a Docker image called `aglover/galoshe` -- run `docker ps` after this command finishes and you'll see it. 

Firing it up is as easy as:

```
$ docker run <image id>
```

Pretty easy, yeah?