Symfony 4 App
===========
This app will setup initial symfony 4 environment ready for development by using docker containers.


# Install

- Clone this repository to your local machine.
- Run `docker network create sf4` to create sf4 docker network
- Run `docker-compose up --build`

# Docker Containers

Build command `docker-compose up --build` will create following docker containers for you in sf4 network 
- sf4_nginx
- sf4_php
- sf4_portainer
- sf4_mysql
- sf4_redis

# Docker

The service uses docker-compose which will host a local containerised environment for the application.

Run `docker-compose up` from the root directory and this will build the application containers, start the webserver and PHP, install composer and run any migrations.

You can then simply view `http://localhost::8081` in your browser.

# Portainer

Portainer is a UI which allow you to easily manage your different Docker environments.
You can view your docker stacks and contrainer by opening `http://0.0.0.0:8888` in your browser. Default user is `admin` and password is `password`

# Running Commands

If you need to run commands on the container you can open a shell with `docker exec -it  sf4_php sh` to access php directly.

