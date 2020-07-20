# Docker

## Docker build
```bash
docker build --name [DOCKER_IMAGE_NAME] .
```

## Docker run
```bash
docker run -d \
--name postgres-server \
-p 5432:5432
-e POSTGRES_PASSWORD=[MY_PASSWORD] \
-e PGDATA=/var/lib/postgresql/data/pgdata \
-v $PWD/data:/var/lib/postgresql/data \
[DOCKER_IMAGE_NAME]
```