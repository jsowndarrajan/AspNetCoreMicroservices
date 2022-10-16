# .Net Microservices
This repository contains sample e-commerce application and it is built for developers who keen to develop applications using microservices architecture and all other software engineering best practices.

## Prerequisites
### Docker Desktop
The docker `linux` container is extensively used in this repository to build and execute the application. The docker desktop is available for following operating systems: Linux, Mac, and Windows. Here is the [download Link.](https://www.docker.com/products/docker-desktop/)

### IDE
Any .NET IDEs can be used for code development. Some of the most commonly used .NET IDEs download link listed below:
* [Visual Studio](https://visualstudio.microsoft.com/vs/)
* [JetBrains Rider](https://www.jetbrains.com/rider/)
* [Visual Studio Code](https://code.visualstudio.com/download)

## Setup Instructions
* Clone or download this repository
* Make sure the Docker desktop is running locally
* Open a Windows terminal in the `src` folder
* Execute the following command to run the application

```
docker-compose up -d
```
* Run the following command to stop and remove the running docker containers
```
docker-compose down
```

## Microservices
### Catalogue API
* [Swagger](http://localhost:9001/swagger/index.html)
* [Mongo Express](http://localhost:9003)