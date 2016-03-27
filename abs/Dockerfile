FROM fellah/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

USER root

RUN pacman -Sy --noconfirm fakeroot && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

ADD makepkg.conf /etc/makepkg.conf

USER fellah
