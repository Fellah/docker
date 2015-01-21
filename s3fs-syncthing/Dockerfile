FROM fellah/s3fs

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ADD https://github.com/syncthing/syncthing/releases/download/v0.10.21/syncthing-linux-amd64-v0.10.21.tar.gz /usr/src/syncthing-linux-amd64-v0.10.21.tar.gz

RUN tar -zxf /usr/src/syncthing-linux-amd64-v0.10.21.tar.gz -C /opt && \
	mv /opt/syncthing-linux-amd64-v0.10.21 /opt/syncthing && \
	ln -s /opt/syncthing/syncthing /usr/local/bin

VOLUME /etc/syncthing

CMD /bin/bash
