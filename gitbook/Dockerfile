FROM node

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN npm install -g gitbook-cli && \
 	npm cache clear

WORKDIR /srv/gitbook
VOLUME /srv/gitbook

CMD /usr/local/bin/gitbook serve
