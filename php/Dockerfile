FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN apt-get update -y && \
	apt-get install -y apache2 php5 php5-xdebug && \
	install --directory --owner=www-data --group=www-data /var/log/xdebug

COPY xdebug.ini /etc/php5/mods-available/xdebug.ini

WORKDIR /var/log/xdebug

CMD apache2ctl -D FOREGROUND
