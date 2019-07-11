# Quickstart: Compose and WordPress

You can use Docker Compose to easily run WordPress in an isolated environment built with Docker containers.
This quick-start guide demonstrates how to use Compose to set up and run WordPress. Before starting,
make sure you have Compose installed.

## Clone the Real World Docker Examples
```
cd ~
git clone https://github.com/DockerJamaica/Docker-Real-World-Examples.git
```

## Create a project folder

- Create an empty project directory
```bash
mkdir wordpress-docker
cd wordpress-docker
```
- Copy the docker-compose.yml file to your project space
```bash
cp ~/Docker-Real-World-Examples/Wordpress/NewSite/docker-compose.yml .
```
- Build the project
```bash
docker-compose up -d
```
## Shuting down project

```bash
 docker-compose down
 ```
