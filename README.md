# Simple Docker Task: Running Nginx with Docker

## 1. How to get started

After installing docker, simply run 
```
docker pull seanlowcy/task_a_cs3219:firstcommit
```

Then run 
```
docker images
```
To check if you have pulled the image. You should see the repository name `seanlowcy/task_a_cs3219` Copy the `IMAGE_ID` of that row.

Next run the command
```
docker run -p 80:9090 <IMAGE_ID>
```

The IMAGE_ID is the id of the image that you have pulled previously from `seanlowcy/task_a_cs3219`. ```-p``` here refers to port. We are simply exposing port 80 (standard HTTP port) of the web server run by Nginx to the port 9090 on our host machine.

Upon successfully running the docker image, go to `http://localhost:9090` and you should see this image (below)

![Image of success deployment of Docker container](https://github.com/seanlowcy77/Simple_Docker_File/blob/master/Images/Docker_Success_pic.png)

## 2. More about Docker Hub

The repository on Docker Hub can be viewed below
https://hub.docker.com/repository/docker/seanlowcy/task_a_cs3219/general

Docker Hub is a hosted repository service provided by Docker. On Docker Hub, we can find, use and share container images. For example, we are able to use and pull images from software such as Ubuntu and Postgres which is extremely useful. In addition, we can also store our own images like how I have done on Docker Hub. A tutorial on how to push images is available below!

https://ropenscilabs.github.io/r-docker-tutorial/04-Dockerhub.html


### a. How Docker Hub looks like

![Image of Docker Hub](https://github.com/seanlowcy77/Simple_Docker_File/blob/master/Images/Docker_Hub_pic.png)


### 3. Versions

This Dockerfile was created and run on:
1. Docker - version 19.03.13