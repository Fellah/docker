# Syncthing Image

Run container:

```
$ docker run \
	-p 8384:8384 \
	-p 22000:22000 \
	-p 22026:22026 \
	-v /etc/syncthing:/root/.config/syncthing \
	-v /srv/syncthing:/srv \
	fellah/syncthing
```
