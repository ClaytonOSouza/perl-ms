FROM debian:10.10-slim

COPY . /opt/app

ENV REDIS_SERVER=127.0.0.1
ENV REDIS_PORT=6379
#ENV REDIS_PASSWORD=

RUN apt-get update && apt-get install -y perl cpanminus make gcc

WORKDIR /opt/app

RUN cpanm --installdeps .

CMD plackup bin/app.psgi
