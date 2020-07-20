# Docker

## Docker build
```docker
docker build --name [DOCKER_IMAGE_NAME] .
```

## Docker run
```docker
docker run -d \
--name postgres-server \
-e POSTGRES_PASSWORD=[MY_PASSWORD] \
-e PGDATA=/var/lib/postgresql/data/pgdata \
-v /custom/mount:/var/lib/postgresql/data \
[DOCKER_IMAGE_NAME]
```