FROM node

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN npm install -g gitbook-cli && \
	gitbook install && \
 	npm cache clear

WORKDIR /srv/gitbook
VOLUME /srv/gitbook

EXPOSE 4000 35729

CMD /usr/local/bin/gitbook serve
