FROM ubuntu

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

# Set the env variable DEBIAN_FRONTEND to noninteractive.
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
	apt-get install -y --no-install-recommends rsync && \
	apt-get autoremove -y && \
	apt-get clean && apt-get autoclean && \
	rm -rf /tmp/* /var/lib/{apt,cache,dpkg,log}/* && \

CMD /usr/bin/rsync /srv/src/ /srv/dest
