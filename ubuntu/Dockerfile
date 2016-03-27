FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ENV DOCKER true

RUN apt-get update &&\
	apt-get -y upgrade &&\
	apt-get -y install xdg-user-dirs

RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/sudo &&\
	useradd --uid 1000 --user-group --create-home fellah &&\
	gpasswd --add fellah sudo

USER fellah

RUN xdg-user-dirs-update

WORKDIR /home/fellah
