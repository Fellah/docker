# Reverse Proxy

```
$ docker run \
	-p 80:80 \
	-p 443:433 \
	-v ./default.conf:/etc/nginx/conf.d/default.conf \
	-v ./http:/src/http \
	--rm rproxy nginx
```
