# S3FS and Syncthing Docker Image

Run container:

```
$ docker run \
	-p 80:80 \
	-p 22000:22000 \
	-p 22026:22026 \
	-v /etc/syncthing:/etc/syncthing \
	--rm --name=s3fs-syncthing fellah/s3fs-syncthing
```
