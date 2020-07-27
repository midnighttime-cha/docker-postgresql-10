# Docker

## Docker login
```bash
cat ~/GH_TOKEN.txt | docker login https://docker.pkg.github.com -u [GITHUB_USERNAME] -p [GITHUB_PASSWORD]
```

## Docker build
```bash
docker build -t docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server .
```

## Docker push
```bash
docker push docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server
```

## Docker run
```bash
docker run -d \
--name postgresql-server \
--restart=always \
-p 5432:5432 \
-v data:/var/lib/postgresql/data \
docker.pkg.github.com/midnighttime-cha/docker-postgresql-10/postgres-server
```