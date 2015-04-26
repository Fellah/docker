FROM ubuntu:14.04

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

VOLUME /mnt/sync

ADD https://github.com/syncthing/syncthing/releases/download/v0.11.1/syncthing-linux-amd64-v0.11.1.tar.gz /usr/src/

RUN tar -zxf /usr/src/syncthing-linux-amd64-v0.11.1.tar.gz -C /opt && \
	ln -s /opt/syncthing-linux-amd64-v0.11.1/syncthing /usr/local/bin

CMD /usr/local/bin/syncthing
