# Box.com Image Container

Secret file should be:

`/etc/davfs2/secrets`

https://dav.box.com/dav [login] [password]

Run container:

```
$ docker run -v /path/secrets:/etc/davfs2/secret --privileged box mount /mnt/box
```
