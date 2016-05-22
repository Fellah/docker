FROM node:6-slim

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ARG version=3.0.0

LABEL version=$version

RUN npm install -g gitbook-cli && gitbook fetch ${version} &&\
	npm cache clear &&\
	rm -rf /tmp/*

WORKDIR /srv/gitbook

VOLUME /srv/gitbook /srv/html

EXPOSE 4000 35729

CMD /usr/local/bin/gitbook serve
