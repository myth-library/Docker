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

<br />

## COPY & ADD commands in Dockerfile

```dockerfile
# Absolute paths
FROM node:14.16.0-alpine3.13
COPY package.json README.md /app/
```

```dockerfile
FROM node:14.16.0-alpine3.13
COPY package*.json /app/
```

```dockerfile
# Relative paths
FROM node:14.16.0-alpine3.13
WORKDIR /app
COPY . .
```

```dockerfile
FROM node:14.16.0-alpine3.13
WORKDIR /app
COPY ["hello world.txt", "."]
```

```dockerfile
FROM node:14.16.0-alpine3.13
WORKDIR /app
COPY . .
ADD https://..../data.json .
```

```dockerfile
FROM node:14.16.0-alpine3.13
WORKDIR /app
COPY . .
ADD data.zip .
```

<br />

## Simple Dockerfile for React application

```dockerfile
FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser —S -G app app
USER app
WORKDIR /app
COPY . .
RUN npm install
ENV API_URL=http://api/myapp.com/
# ENV API_URL http://api/myapp.com/   <-- Old way
EXPOSE 3000  # exposing ports
# CMD npm start  <-- shell form
CMD ["npm", "start"]  # Execute form
```

### Optimized Dockerfile

```dockerfile
FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser —S -G app app
USER app
WORKDIR /app
COPY package*.json .
RUN npm install
COPY . .
ENV API_URL=http://api/myapp.com/
EXPOSE 3000  # exposing ports
CMD ["npm", "start"]  # Execute form
```
