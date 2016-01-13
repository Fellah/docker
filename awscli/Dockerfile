FROM ubuntu

RUN apt-get update -y && \
	apt-get install -y python2.7 && \
	apt-get install -y python-pip && \
	pip install awscli && \
	useradd --uid 1000 --user-group --create-home fellah

USER fellah

WORKDIR /home/fellah
