FROM ubuntu:latest

RUN apt-get update -y && \
	apt-get -y install python2.7 python-pip bash-completion && \
	pip install awscli && \
	useradd --uid 1000 --user-group --create-home fellah

RUN install --directory /etc/bash_completion.d && \
	cp /usr/local/bin/aws_bash_completer /etc/bash_completion.d

USER fellah

WORKDIR /home/fellah
