# GitBook Image

Run container:

```
$ docker run -p 80:4000 -v /srv/gitbook fellah/gitbook
```

`4000` – GitBook default service port.

`35729` – Live reload server port.

`/srv/gitbook` – Default working directory for GitBook container.


## Build Static Website

```
$ docker run -v /srv/gitbook -v /srv/html fellah/gitbook gitbook build . /srv/html
```

## Links

[GitHub: GitBook](https://github.com/GitbookIO/gitbook)

[GitBook Toolchain Documentation](http://toolchain.gitbook.com)
