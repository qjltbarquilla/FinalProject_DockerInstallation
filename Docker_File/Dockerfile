FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y \
    apache2 \
    mariadb-server \
    && rm -rf /var/lib/apt/lists/*

RUN echo "ServerName localhost" | tee /etc/apache2/httpd.conf

EXPOSE 80 3306

CMD service mariadb start && apache2ctl -D FOREGROUND
