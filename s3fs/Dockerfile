FROM ubuntu:14.04

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && \
	apt-get install -y libfuse-dev libcurl4-openssl-dev libxml2-dev mime-support && \
	apt-get install -y build-essential automake libtool wget && \
	wget https://github.com/s3fs-fuse/s3fs-fuse/archive/v1.78.tar.gz -O /usr/src/s3fs-fuse-1.78.tar.gz && \
	tar -xzv -C /usr/src -f /usr/src/s3fs-fuse-1.78.tar.gz && \
	cd /usr/src/s3fs-fuse-1.78 && \
	./autogen.sh && \
	./configure --prefix=/usr && \
	make && \
	make install && \
	apt-get purge -y build-essential automake libtool wget && \
	apt-get autoremove -y && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/* && \
	rm -rf /usr/src/s3fs-fuse*

VOLUME ["/mnt/s3fs"]
