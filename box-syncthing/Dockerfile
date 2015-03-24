FROM fellah/box

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN apt-get update && \
	apt-get install -y --no-install-recommends rsync && \
	apt-get clean autoclean && \
	apt-get autoremove -y && \
	rm -rf /var/lib/{apt,dpkg,cache,log}/

ADD https://github.com/syncthing/syncthing/releases/download/v0.10.29/syncthing-linux-amd64-v0.10.29.tar.gz /usr/src/

RUN tar -zxf /usr/src/syncthing-linux-amd64-v0.10.29.tar.gz -C /opt && \
	ln -s /opt/syncthing-linux-amd64-v0.10.29/syncthing /usr/local/bin

CMD mount /mnt/box && syncthing
