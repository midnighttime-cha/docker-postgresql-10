FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y --no-install-recommends \
  virtualenv \
  python-pip \
  libpq-dev python-dev

RUN wget https://ftp.postgresql.org/pub/pgadmin/pgadmin4/v1.4/pip/pgadmin4-1.4-py2.py3-none-any.whl
RUN pip install pgadmin4-1.4-py2.py3-none-any.whl

RUN echo "SERVER_MODE = False" >> lib/python2.7/site-packages/pgadmin4/config_local.py

EXPOSE 5050

CMD [ "python", "lib/python2.7/site-packages/pgadmin4/pgAdmin4.py" ]