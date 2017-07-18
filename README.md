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
