FROM node

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

VOLUME /mnt/gitbook

RUN npm install -g gitbook-cli && \
 	npm cache clear

WORKDIR /mnt/gitbook

ENTRYPOINT /usr/local/bin/gitbook serve
