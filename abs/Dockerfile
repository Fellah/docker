FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/* && \
	pacman-key --init && \
	pacman-key --populate archlinux && \
	pacman-key --refresh-keys && \
	pacman -Syyu --noconfirm && \
	pacman-db-upgrade && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

RUN pacman -Sy --noconfirm fakeroot && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

RUN useradd --create-home abs

USER abs

VOLUME /home/abs

WORKDIR /home/abs

CMD bash
