FROM fellah/ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

USER root

RUN apt-get -y install software-properties-common && \
	apt-add-repository -y ppa:ansible/ansible && \
	apt-get update && \
	apt-get -y install ansible sshpass

USER fellah
