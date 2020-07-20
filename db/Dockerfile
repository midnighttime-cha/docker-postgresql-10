FROM postgres:10.13

RUN apt update

RUN sed -i -e"s/^#listen_addresses =.*$/listen_addresses = '*'/" /etc/postgresql/10.13/main/postgresql.conf
RUN sed -i -e"s/^max_connections = 100.*$/max_connections = 1000/" /etc/postgresql/10/main/postgresql.conf
RUN sed -i -e"s/^shared_buffers = 128MB.*$/shared_buffers = 3GB/" /etc/postgresql/10/main/postgresql.conf
RUN echo "host    all    all    0.0.0.0/0    md5" >> /etc/postgresql/10/main/pg_hba.conf

VOLUME ["postgresql-data", "/var/lib/postgresql/data"]

EXPOSE 5432

CMD ["postgres"]