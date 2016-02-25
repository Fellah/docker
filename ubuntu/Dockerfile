FROM ubuntu:latest

RUN apt-get update &&\
	apt-get -y upgrade

RUN echo '%sudo ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/sudo &&\
	useradd --uid 1000 --user-group --create-home fellah &&\
	gpasswd --add fellah sudo

USER fellah

WORKDIR /home/fellah
