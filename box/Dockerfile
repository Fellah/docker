FROM ubuntu:14.04

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN apt-get update && \
	apt-get install -y davfs2 && \
	mkdir /mnt/box

COPY fstab /etc/fstab

CMD mount /mnt/box
