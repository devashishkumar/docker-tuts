## Docker Commands

| Purpose | Command |
| ------ | ------ |
| docker pull from repo | docker pull containername |
| pull specific version | docker pull containername:versionname(tag name) |
| pull and run docker container | docker run -d containername |
| run docker container in specific port | docker run --name angulardockercontainer -d -p 8088:80 angulardockercontainer|
| create docker container | docker build -t containername .|
| run docker container | docker run -d containername |
| list all running container | docker ps |
| stop any existing running container | docker stop containerid |
| start previously stopped container | docker start containerid |
| docker running containers history | docker ps -a |
| tag docker for specific version| docker tag sourceimage:tagversion codewithashish/targetimage:version|
| push tagged version to docker hub | docker push codewithashish/targetimage:version|

## here codewithashish is a dockerid