# Dockerfile Instructions

## What includes inside a Dockerfile

- A Dockerfile contains instructions for building an image

<br />

## Simple Dockerfile

- typically starts with a `base image (FROM)`

```dockerfile
FROM node:alpine
COPY . /app
CMD node /app/app.js
```

```dockerfile
FROM node:alpine
COPY . /app
WORKDIR /app
CMD node app.js
```
