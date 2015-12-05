# Syncthing Image

## Use

```
$ docker run \
	-p 8384:8384 \
	-p 22000:22000 \
	-v /path/to/config:/root/.config/syncthing \
	-v /path/to/sync/data:/root/sync/data \
	fellah/syncthing
```
