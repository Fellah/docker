FROM node

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN npm install -g gitbook-cli && \
 	npm cache clear && \
	gitbook install

WORKDIR /srv/gitbook
VOLUME /srv/gitbook

EXPOSE 4000 35729

CMD /usr/local/bin/gitbook serve
