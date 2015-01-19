# S3FS Docker Image

Run container:

```
$ docker run \
	-v /path/to/host/passwd-s3fs:/etc/passwd=s3fs \
	--rm --name=s3fs fellah/s3fs
```
