FROM node:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="2.5.0"

RUN npm install -g gitbook-cli && gitbook versions:install 2.5.0 && \
	apt-get clean autoclean && npm cache clear && \
	rm -rf /tmp/* /var/lib/{apt,dpkg,cache,log}/*

WORKDIR /srv/gitbook

VOLUME /srv/gitbook /srv/html

EXPOSE 4000 35729

CMD /usr/local/bin/gitbook serve
