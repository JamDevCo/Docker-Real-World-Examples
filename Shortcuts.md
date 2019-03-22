## Install Docker

#### Installing Docker on Debian based distro
```bash
sudo apt-get install docker
```

### Installing Docker on Windows

Go to https://hub.docker.com/editions/community/docker-ce-desktop-windows, download and install it.
Once Docker is installed, use Docker Interactive Window or Powershell to use the following commands.


## Login to docker

To use Docker's public images, you must have a Docker ID or account, 
go to https://hub.docker.com/ and register your account if you don't have one as yet.
Otherwise, run the following command:

```bash

docker login
```

## Checking if there’s any container running

```bash
docker ps
```

List all containers, event if they aren’t running

```bash
docker ps -a
```

## Running a container
Docker run creates a new container from the docker image and starts the container
docker run tutum/hello-world

### Naming a container
```bash
docker run --name web1 tutum/hello-world
```

#### Running a docker container on a particular port
```bash
# docker run --name web2 -p exposePORTt:localPort tutum/hello-world
docker run --name web2 -p 8080:80 tutum/hello-world
```

#### Running docker containers in the background using daemon
```bash
docker run -d --name web3 -p 8080:80 tutum/hello-world
docker run -d --name web4 -p 8081:80 tutum/hello-world
```

## Get logs for a container
```bash
docker logs web3
```

### Get all logs for all containers
```bash
for dlog in `docker ps -a -q`; do docker logs $dlog; done
```

## Stopping a docker container
```bash
docker stop web3
```

### Stopping more than one docker container
```bash
docker stop $(docker ps -a -q)
```


## Starting a docker container
```bash
docker start web3
```

## Removing a container

```bash
# docker rm <container-name>
docker rm web3
````

### Removing all containers
```bash
docker rm $(docker ps -a -q)
```

Stop and remove all containers
```bash
docker rm $(docker ps -a -q) & docker stop $(docker ps -a -q)
```

## List docker images
```bash
docker images
```

## Remove a docker image
```
docker rmi wordpress
```

### Remove all images
```
docker rmi $(docker images -q)
```

