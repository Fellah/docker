FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="0.12.6"

ADD https://github.com/syncthing/syncthing/releases/download/v0.12.6/syncthing-linux-amd64-v0.12.6.tar.gz /tmp/

RUN mkdir /opt/syncthing && \
	tar -zxf /tmp/syncthing-linux-amd64-v0.12.6.tar.gz -C /opt/syncthing  --strip-components 1 && \
	ln -s /opt/syncthing/syncthing /usr/local/bin && \
	useradd --create-home syncthing

USER syncthing

EXPOSE 8384 22000

VOLUME /home/syncthing

WORKDIR /home/syncthing

CMD syncthing
