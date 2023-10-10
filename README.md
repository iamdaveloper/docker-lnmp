# Linux Nginx Mysql PHP 4 in 1 Docker Image

## Build docker 
```
>>>>> Create a virtual network for development
>>>>> docker network create [fill the good name] --subnet=172.19.0.0/16
$ docker network create development --subnet=172.19.0.0/16

>>>>> Rebuild the docker image if dockerfile or env has changed.
$ docker-compose up -d --build nginx php82

>>>>> Just restart the services if config has changed.
$ docker-compose restart nginx php82
```

## Build a new project

1. clone this docker to your project  
`git clone https://github.com/iamdaveloper/docker-lnmp.git`

2. copy the .env  
`cp .env.example .env`

3. basic setting  
app_name = your domain name  (e.g: app_name = 'localhost' => `https://localhost/`)  
change `WEB_ROOT_PATH` to `YOURPROJECTROOTPATH`  (e.g: `/var/www/html/helloworld/`)  

4. nginx config  
`default.conf`  
`server_name = YOURDOMAINNAME`