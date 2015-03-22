FROM fellah/box

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

# Set the env variable DEBIAN_FRONTEND to noninteractive
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
	apt-get install -y --no-install-recommends rsync && \
	apt-get clean autoclean && \
	apt-get autoremove -y && \
	rm -rf /var/lib/{apt,dpkg,cache,log}/

CMD mount /mnt/box && \
	rsync -rtv --del $FLAGS $SRC $DEST
