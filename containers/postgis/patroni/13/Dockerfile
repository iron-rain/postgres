FROM postgis/postgis:13-3.1

ARG DEBIAN_FRONTEND="noninteractive"

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install pgbackrest python3 python3-pip -y && \
    pip3 install schedule patroni[kubernetes] psycopg2-binary


RUN chown postgres /etc/pgbackrest.conf && \
    chown postgres /var/log/pgbackrest && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    ln -s /usr/bin/pip3 /usr/bin/pip

RUN mkdir /home/postgres && \
    chown postgres /home/postgres && \
    chown postgres /var/lib/pgbackrest && \
    mkdir /archive/ && \
    chown postgres /archive      