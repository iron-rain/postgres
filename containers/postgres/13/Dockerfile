FROM postgres:13

ARG DEBIAN_FRONTEND="noninteractive"

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install pgbackrest python3 python3-pip -y && \
    pip3 install schedule

RUN chown postgres /etc/pgbackrest.conf && \
    chown postgres /var/log/pgbackrest && \
    ln -s /usr/bin/python3 /usr/bin/python && \
    ln -s /usr/bin/pip3 /usr/bin/pip