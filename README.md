# Docker Images

## What includes in Docker images?

- Everything (all the files & configurations) an application needs to run
  - cut-down OS
  - Third-party libraries
  - Application files
  - Environment variables

<br/>

## What is a container?

- Container = an instance of the docker image
- Also, an isolated environment
  - e.g., Changes of the container A not visible to container B

<br/>

## How to choose correct base image for application?

- <https://docs.docker.com/samples/>
- We can choose correct base image based on Databases, Framework, Languages etc.
