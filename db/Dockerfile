FROM postgres:10.13-alpine

RUN apk update
RUN apk add nano

RUN sed -i -e"s/^#listen_addresses =.*$/listen_addresses = '*'/" /var/lib/postgresql/data/postgresql.conf
RUN echo "host    all    all    0.0.0.0/0    md5" >> /var/lib/postgresql/data/pg_hba.conf
RUN sed -i -e"s/^max_connections = 100.*$/max_connections = 1000/" /var/lib/postgresql/data/postgresql.conf
RUN sed -i -e"s/^shared_buffers = 128MB.*$/shared_buffers = 3GB/" /var/lib/postgresql/data/postgresql.conf

VOLUME ["postgresql-data", "/var/log/postgresql"]

EXPOSE 5432

CMD ["postgres"]