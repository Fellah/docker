FROM fellah/s3fs-syncthing

MAINTAINER Roman Krivetsky <r.krivetsky@gmail.com>

CMD s3fs dixet /mnt/s3fs \
    	-o nomultipart \
    	-o url=https://storage.googleapis.com && \
    syncthing --home=/etc/syncthing
