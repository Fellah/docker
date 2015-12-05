# Syncthing Image

## Use

```
$ docker run \
	-p 8384:8384 \
	-p 22000:22000 \
	-v /path/to/config:/home/root/.config/syncthing \
	-v /path/to/syncthing:/home/root/syncthing \
	fellah/syncthing
```
