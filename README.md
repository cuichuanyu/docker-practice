[![Build Status](https://travis-ci.org/shawnkoon/docker-practice.svg?branch=master)](https://travis-ci.org/shawnkoon/docker-practice)
# docker-practice
Docker practice to get familiarized with docker.

# To run

## v1
`$ docker build -t shawnkoon/docker_app:1.00 .`

`$ docker run -d -p 5000:5000 --name dockerapp shawnkoon/docker_app:1.00`

Search `localhost:5000` to access website.

## v2
`$ docker build -t shawnkoon/docker_app:2.00 .`

`$ docker run -d --name redisapp redis:3.2.0`

`$ docker run -d -p 5000:5000 --link redisapp --name dockerapp shawnkoon/docker_app:2.00`

## v3
`$ docker-compose up -d`

`$ docker-compose logs`

`$ docker-compose down`

## v4
`$ docker-compose up -d`

`$ docker network inspect dockerpractice_shawnkoon_network`

`$ docker inspect dockerapp | grep 'network'`

`$ docker inspect redisapp | grep 'network'`

`$ docker-compose down`

## v5

`$ docker-compose up -d`

`$ docker-compose ps`

`$ docker-compose run dockerapp python test.py`

`$ docker-compose down`
