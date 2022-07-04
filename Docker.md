# Docker Notes

### Docker

- To publish nginx container:
```sh
docker container run --publish 80:80 --detach --name webhost nginx
```
- To list all docker containers running
```sh
docker container ls -a
```
- Detach arg is used to run container in the background
- To list all running containers
```sh
docker container ls
```
- To stop container(can have multiple container names) => executes SIGTERM on processes
```sh
docker container stop <CONTAINER_ID>
```
- To kill container(can have multiple container names) => executes SIGKILL on processes => container only has 10 secs to stop
```sh
docker container kill <CONTAINER_ID>
```
- To remove docker containers(can have multiple container names)
```sh
docker container rm <CONTAINER_IDS>
```
- To force remove containers(can have multiple container names)
```sh
docker container rm -f <CONTAINER_IDS>
```
- Read difference between stop and remove [Stackoverflow](https://stackoverflow.com/a/33362991/7975209)
- To list all the logs of container
```sh
docker container logs webhost
```
- To list process list in one container
```sh
docker container top
```
- To list details of one container config
```sh
docker container inspecct <CONTAINER_NAME>
```
- To list all container stats
```sh
docker container stats
```
- To start a new docker container interactvely
```sh
docker container run -it
```
- To run additional commant in existing container
```sd
docker container exec -it <CONTAINER_NAME> <COMMAND>
```
- To show docker container port mapping
```sh
docker container port <CONTAINER_NAME>
```
- Docker images are layer based, cached and read only once built
- To remove docker containers, first stop the container if it is in running state
```sh
docker stop <CONTAINER_NAME>

docker rm <MULTIPLE_CONTAINER_NAMES>
```
- To list docker images
```sh
docker images
```
- To remove images (images only gets removed if they are not being used by any container)
```sh
docker rmi <IMAGE_IDS>
```
- To remove all dangling images
```sh
docker image prune
```

### Docker Network
- To list all the docker networks
```sh
docker network ls
```
- To inspect any particular network
```sh
docker network inspect <NETWORK_NAME>
```
- To create a new network
```sh
```
- Docker containers should not rely on ip addresses for communication, therefore they use DNS(container names) to find and communicate with other containers



# Kubernetes Notes

### Kubernetes