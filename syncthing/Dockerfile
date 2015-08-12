FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="0.11.19"

ADD https://github.com/syncthing/syncthing/releases/download/v0.11.19/syncthing-linux-amd64-v0.11.19.tar.gz /tmp/

RUN mkdir /opt/syncthing && \
	tar -zxf /tmp/syncthing-linux-amd64-v0.11.19.tar.gz -C /opt/syncthing  --strip-components 1 && \
	ln -s /opt/syncthing/syncthing /usr/local/bin && \
	useradd --create-home --no-user-group --uid 1000 syncthing && \
	install -d -o syncthing -g users /srv/syncthing && \
	install -d -o syncthing -g users /home/syncthing/.config/syncthing

EXPOSE 8384 22000

USER syncthing

VOLUME /srv/syncthing /home/syncthing/.config/syncthing

WORKDIR /srv/syncthing

CMD syncthing
