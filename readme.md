## Docker

## Containers Vs Images

-- Docker Image is a set of files which has no state, whereas Docker Container is the instantiation of Docker Image. Docker Container is the run time instance of images.

-- Images can exist without containers, but a container needs to run an image to exist. Therefore, containers are dependent on images and use them to construct a run-time environment and run an application. The two concepts exist as essential components (or rather phases) in the process of running a Docker container


## Docker Commands

| Purpose | Command |
| ------ | ------ |
| docker pull from repo | docker pull containername |
| pull specific version | docker pull containername:versionname(tag name) |
| pull and run docker container from public repo | docker run -d containername |
| run docker container in specific port | docker run --name angulardockercontainer -d -p 8088:80 angulardockercontainer|
| create docker container | docker build -t containername .|
| run docker container | docker run -d containername |
| list all running container | docker ps |
| list all docker images | docker images |
| stop any existing running container | docker stop containerid |
| start previously stopped container | docker start containerid |
| docker running containers history | docker ps -a |
| tag docker for specific version| docker tag sourceimage:tagversion codewithashish/targetimage:version|
| push tagged version to docker hub | docker push codewithashish/targetimage:version|

## here codewithashish is a docker-hub dockerid


## Docker containers trouble shooting

| Purpose | Command |
| ------ | ------ |
| list all containers | docker ps |
| list container logs | docker logs containerid/containername |
| run container with the different name | docker run -d -p9090:8080 --name newname actualcontainername |
| enter into any particular container directory (containerid) | docker exec -it containerid /bin/bash |
| enter into any particular container directory (containername) | docker exec -it containername /bin/bash |


## docker run Vs docker start

-- Docker run is use to create container with an image
-- docker start is to start/restart a container