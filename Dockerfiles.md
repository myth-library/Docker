# Docker Files

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
