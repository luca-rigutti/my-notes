# Docker

## Commands

### `docker pull`

To download the image

### `docker ps`

To show all the container is running

if you want to view also the contaniner live, you need to add `-a` command.

### `docker run`

For setting the port: `-pLocalPort:PortInsideContaniner`

For detach: `-d`

### `docker log`

with contanier id or name

### `docker exec`

With `-it` argument for have interactive shell

### `docker network`

## Docker image


### An example

```yaml
FROM Image

ENV variable 

WORKDIR directoryExample

RUN Command

COPY sourceHost targetHost

CMD Command

```
## Docker container

### Docker compose

### An example

```yaml

version: '3' #Docker compose version
services:
	nameOfService:
    	Image: NameofImage
        ports:
        	- ExposePort:LocalPort
        environment:
           	- Variable = 'value'
        volumes:
        - db-data:/var/lib/mysql/data
        
volumes:
	db-data

```

## Disable auto restart

`docker update --restart=no my-container`

From https://stackoverflow.com/questions/37599128/docker-how-do-you-disable-auto-restart-on-a-container

---

This information are the resource collected from online and my colleague.

This is some resource I used:

[Docker Tutorial for Beginners [FULL COURSE in 3 Hours]](https://www.youtube.com/watch?v=3c-iBn73dDE)