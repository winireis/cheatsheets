# Docker Commands and Tips
## Commands
### List all images
```
$ docker images -a
```
### List all containers
```
$ docker ps -a
```
### List all volumes
```
$ docker volume ls
```
### Purge **ALL** stopped images, containers, volumes and networks from your machine
Only use this command in your development environment.
```
$ docker system prune -a
```
## Tips
[Oficial Docker Image repositories](https://hub.docker.com/explore/)
