# Docker

## Docker build
```bash
docker build -t docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server .
```

## Docker push
```bash
cat ~/GH_TOKEN.txt | docker push docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server .
```

## Docker run
```bash
docker run -d \
--name postgresql-server \
--restart=always \
-p 5432:5432 \
-e POSTGRES_USER=postgres \
-e POSTGRES_PASSWORD=[PASSWORD] \
-e POSTGRES_DB=postgres \
-e PGDATA=/var/lib/postgresql/data/pgdata \
-v data:/var/lib/postgresql/data \
docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server
```