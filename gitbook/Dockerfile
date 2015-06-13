FROM node

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

VOLUME /srv/gitbook

RUN npm install -g gitbook-cli && \
 	npm cache clear

WORKDIR /srv/gitbook

CMD /usr/local/bin/gitbook serve
