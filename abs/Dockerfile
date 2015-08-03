FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/*
RUN pacman-key --init
RUN pacman-key --populate archlinux
RUN pacman-key --refresh-keys
RUN pacman -Syyu --noconfirm
RUN pacman-db-upgrade
RUN pacman -Sy --noconfirm fakeroot

VOLUME /srv/abs

RUN useradd --create-home --no-user-group --uid 1000 fellah
USER fellah

VOLUME /srv/abs
WORKDIR /srv/abs
