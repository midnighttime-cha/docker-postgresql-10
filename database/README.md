# Docker

## Docker build
```bash
docker build -t docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server .
```

## Docker push
```bash
~/GH_TOKEN.txt docker push docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server .
```

## Docker run
```bash
docker run -d \
--name postgresql-server \
-p 5432:5432 \
-v postgresql:/etc/postgresql \
-v logs:/var/log/postgresql \
-v lib:/var/lib/postgresql \
docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server
```