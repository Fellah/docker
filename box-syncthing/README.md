# Syncthing Image Container

DavFS secrets file `/etc/davfs2/secrets`.

`/etc/davfs2/secrets`

	https://dav.box.com/dav [login] [password]

Syncthing data `/root/.config/syncthing`.

Run container:

```
$ docker run \
	-p 22000:22000 \
	-p 22026:22026 \
	-v /etc/davfs/secrets \
	-v /root/.config/syncthing \
	--privileged \
	--rm --name=syncthing fellah/box-syncthing
```
