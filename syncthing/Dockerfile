FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ADD https://github.com/syncthing/syncthing/releases/download/v0.11.7/syncthing-linux-amd64-v0.11.7.tar.gz /usr/src/

RUN tar -zxf /usr/src/syncthing-linux-amd64-v0.11.7.tar.gz -C /opt && \
	ln -s /opt/syncthing-linux-amd64-v0.11.7/syncthing /usr/local/bin

CMD /usr/local/bin/syncthing -gui-address=0.0.0.0:8384 -no-browser
