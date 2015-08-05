FROM base/archlinux:latest

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

RUN rm -rf /etc/pacman.d/gnupg/* && \
	pacman-key --init && \
	pacman-key --populate archlinux && \
	pacman-key --refresh-keys && \
	pacman -Syyu --noconfirm && \
	pacman-db-upgrade && \
	pacman -Sy --noconfirm fakeroot && \
	rm -rf /tmp/* /var/cache/pacman/pkg/*

RUN useradd --create-home --no-user-group --uid 1000 abs && \
	install --directory --mode=755 --owner=abs --group=users /srv/abs
USER abs

VOLUME /srv/abs
WORKDIR /srv/abs

CMD repo-add repo.db.tar.gz *.pkg.tar.xz
