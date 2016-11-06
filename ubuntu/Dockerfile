FROM ubuntu:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

ENV DOCKER true

RUN apt-get update &&\
	apt-get -y upgrade &&\
	apt-get -y install xdg-user-dirs

RUN useradd --uid 1000 --user-group --create-home fellah

USER fellah

RUN xdg-user-dirs-update

WORKDIR /home/fellah
