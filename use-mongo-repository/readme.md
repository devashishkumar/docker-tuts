### use mongo repository

| Purpose | Command |
| ------ | ------ |
| pull mongo image | docker pull mongo |
| pull mongo-express image | docker pull mongo-express |
| check docker networks | docker network ls |
| create network | docker network create mongo-network |
| start mongo container with username/password | docker run -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME=ashish -e MONGO_INITDB_ROOT_PASSWORD=ashish --name mongodb --net mongo-network mongo|
| start mongo container without username/password | docker run -p 27017:27017 -d --name mongodb --net mongo-network mongo|
| check mongo container command status | docker logs e75eb688d6829f907e49ca6de0bfbe72f95c6f6c0e797bf20a22aed50a304b0c|

### we can start mongo container using docker run command or we can create yaml file to automate these processes using docker compose command

| Purpose | Command |
| ------ | ------ |
| docker compose | docker-compose -f mongo.yaml up |
| docker compose to stop existing container | docker-compose -f mongo.yaml down |