FROM fellah/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

USER root

RUN pacman --sync --refresh --sysupgrade --noconfirm && \
	pacman --sync --refresh --noconfirm fakeroot binutils file && \
	rm --recursive --force /tmp/* /var/cache/pacman/pkg/*

USER fellah
