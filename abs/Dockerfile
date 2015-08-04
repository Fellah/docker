FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/* && \
	pacman-key --init && \
	pacman-key --populate archlinux && \
	pacman-key --refresh-keys && \
	pacman -Syyu --noconfirm && \
	pacman-db-upgrade && \
	pacman -Sy --noconfirm fakeroot

VOLUME /srv/abs
WORKDIR /srv/abs

RUN useradd --create-home --no-user-group --uid 1000 abs
USER abs
