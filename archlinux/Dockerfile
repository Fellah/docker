FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/* && \
	pacman-key --init && \
	pacman-key --populate archlinux && \
	pacman-key --refresh-keys && \
	pacman -Syyu --noconfirm && \
	pacman-db-upgrade && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

RUN pacman -Sy --noconfirm sudo && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

ADD sudoers.d/wheel /etc/sudoers.d/wheel

RUN useradd --create-home fellah && \
	gpasswd --add fellah wheel

USER fellah

VOLUME /home/fellah

WORKDIR /home/fellah

CMD bash
