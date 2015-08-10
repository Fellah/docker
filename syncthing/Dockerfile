FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="0.11.19"

ADD https://github.com/syncthing/syncthing/releases/download/v0.11.19/syncthing-linux-amd64-v0.11.19.tar.gz /tmp/

RUN mkdir /opt/syncthing && \
	tar -zxf /tmp/syncthing-linux-amd64-v0.11.19.tar.gz -C /opt/syncthing  --strip-components 1 && \
	ln -s /opt/syncthing/syncthing /usr/local/bin

EXPOSE 8384 22000

CMD syncthing -gui-address=0.0.0.0:8384 -no-browser
