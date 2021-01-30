FROM ubuntu:20.04

ARG DEBIAN_FRONTEND="noninteractive"

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install pgbackrest -y

RUN groupadd -g 999 pgbackrest && \
    useradd -u 999 pgbackrest -g 999 && \
    chown pgbackrest /etc/pgbackrest.conf && \
    chown pgbackrest /var/log/pgbackrest
