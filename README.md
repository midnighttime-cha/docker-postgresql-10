# Docker

## Docker build
```bash
docker build --name [DOCKER_IMAGE_NAME] .
```

## Docker run
```bash
docker run -d \
--name postgres-server \
-e POSTGRES_PASSWORD=[MY_PASSWORD] \
-e PGDATA=/var/lib/postgresql/data/pgdata \
-v ./data:/var/lib/postgresql/data \
[DOCKER_IMAGE_NAME]
```