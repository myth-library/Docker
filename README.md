# Docker

<br/>

## Table of Contents

1. [How to build a docker image using a Dockerfile](#how-to-build-a-docker-image-using-a-dockerfile)
2. [How to run a docker image](#how-to-run-a-docker-image)

<br/><br/><br/>

## How to build a docker image using a Dockerfile

- command template --> `docker build -t <tag_name> <location_to_dockerfile>`

  - `.` means, current directory

```
docker build -t hello-docker .
```

<br/>

## How to run a docker image

```
docker run hello-docker
```
