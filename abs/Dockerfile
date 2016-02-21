FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/* && \
	pacman-key --init && \
	pacman-key --populate archlinux && \
	pacman-key --refresh-keys && \
	pacman -Syyu --noconfirm && \
	pacman-db-upgrade && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

RUN pacman -Sy --noconfirm sudo fakeroot && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

ADD sudoers.d/wheel /etc/sudoers.d/wheel

RUN useradd --create-home abs && \
	gpasswd -a abs wheel

USER abs

VOLUME /home/abs

WORKDIR /home/abs

CMD bash
