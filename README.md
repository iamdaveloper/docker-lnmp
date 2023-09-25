# Linux Nginx Mysql PHP 4 in 1 Docker Image

```
## Create a virtual network for development 
## docker network create [fill the good name] --subnet=172.19.0.0/16
$ docker network create development --subnet=172.19.0.0/16

## Rebuild the docker image if dockerfile or env has changed.
$ docker-compose up -d --build nginx php82

# Just restart the services if config has changed.
$ docker-compose restart nginx php82