FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="0.11.23"

ADD https://github.com/syncthing/syncthing/releases/download/v0.11.23/syncthing-linux-amd64-v0.11.23.tar.gz /tmp/

RUN mkdir /opt/syncthing && \
	tar -zxf /tmp/syncthing-linux-amd64-v0.11.23.tar.gz -C /opt/syncthing  --strip-components 1 && \
	ln -s /opt/syncthing/syncthing /usr/local/bin && \
	useradd --create-home --no-user-group --uid 1000 syncthing

USER syncthing

EXPOSE 8384 22000

VOLUME /home/syncthing

WORKDIR /home/syncthing

CMD syncthing
