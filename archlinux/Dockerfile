FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

LABEL version="20160221"

RUN pacman-key --refresh-keys && \
	pacman -Syu --noconfirm && \
	pacman-db-upgrade
