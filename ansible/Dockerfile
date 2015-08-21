FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN apt-get -y install software-properties-common && \
	apt-add-repository -y ppa:ansible/ansible && \
	apt-get update -y && \
	apt-get install -y ansible sshpass && \
	useradd -m -N -u 1000 ansible

USER ansible

VOLUME /home/ansible

WORKDIR /home/ansible

CMD bash
