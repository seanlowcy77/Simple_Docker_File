# Simple Docker Task: Running Nginx with Docker

## Some background about Docker...

Typically when running or testing multiple servers or applications on different Operating Systems, if we want to do it on our local machine, we require virtual machines. We can create and run these virtual machines using a hypervisor. However when running each of these virtual machines, we have to allocate a fixed memory and space to them. Thus there is alot of wastage.

Docker fixes that. With Docker, instead of a hypervisor, we have a container engine to manage and create containers. These containers will run the application and all its dependencies and it will use the host operating system. Now the space and memory is not fixed and it will be taken as per the needs of the application so there is no overhead. Thus it becomes very lightweight and fast! In addition, Docker is extremely useful for continuous deployment.

## 1. Contents of Docker Image

This is a simple Docker file: the contents are as below:

```
FROM: nginx

MAINTAINER: sean low
```
What we are doing here is that we are simply pulling the latest version docker image from nginx on Docker Hub and then running it using a command shown below.

## 2. How to get started

After installing docker, simply run 
```
docker pull seanlowcy/task_a_cs3219:firstcommit
```
With the above command, we have pulled the docker image from Docker Hub.
Then run 
```
docker images
```
To check if you have pulled the image successfully. You should see the repository name `seanlowcy/task_a_cs3219` Copy the `IMAGE_ID` of that row.

Next run the command
```
docker run -p 80:9090 <IMAGE_ID>
```

The IMAGE_ID is the id of the image that you have pulled previously from `seanlowcy/task_a_cs3219`. ```-p``` here refers to port. We are simply exposing port 80 (standard HTTP port) of the web server run by Nginx to the port 9090 on our host machine.

Upon successfully running the docker image, go to `http://localhost:9090` and you should see this image (below)!

![Image of success deployment of Docker container](https://github.com/seanlowcy77/Simple_Docker_File/blob/master/Images/Docker_Success_pic.png)

## 3. More about Docker Hub

The repository on Docker Hub can be viewed below
https://hub.docker.com/repository/docker/seanlowcy/task_a_cs3219/general

Docker Hub is a hosted repository service provided by Docker. Think of it as similar to Github. On Docker Hub, we can find, use and share container images. For example, we are able to use and pull images from software such as Ubuntu and Postgres which you can then run yourselves! In addition, we can also store our own images like how I have done on Docker Hub. A tutorial on how to push images is available below!

https://ropenscilabs.github.io/r-docker-tutorial/04-Dockerhub.html


### a. How Docker Hub looks like

![Image of Docker Hub](https://github.com/seanlowcy77/Simple_Docker_File/blob/master/Images/Docker_Hub_pic.png)


### 4. Versions

This Dockerfile was created and run on:
1. Docker - version 19.03.13