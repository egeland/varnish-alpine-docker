# varnish-alpine-docker
![Build Status](https://api.travis-ci.org/thiagofigueiro/varnish-alpine-docker.svg)
![Docker Stars](https://img.shields.io/docker/stars/thiagofigueiro/varnish-alpine-docker.svg?link=https://hub.docker.com/r/thiagofigueiro/varnish-alpine-docker/)
![Docker Pulls](https://img.shields.io/docker/pulls/thiagofigueiro/varnish-alpine-docker.svg?link=https://hub.docker.com/r/thiagofigueiro/varnish-alpine-docker/)

A very small Varnish docker image based on Alpine Linux.

## Environment variables
* `VARNISH_BACKEND_ADDRESS` - host/ip of your backend.  Defaults to 192.168.1.65.
* `VARNISH_BACKEND_PORT` - TCP port of your backend.  Defaults to 80.
* `VARNISH_MEMORY` - how much memory Varnish can use for caching. Defaults to 100M.

## Quick start

Run with defaults:

```bash
docker run -Pit --name=varnish-alpine thiagofigueiro/varnish-alpine-docker
```

Specify your backend configuration:

```bash
docker run -Pit -e VARNISH_BACKEND_ADDRESS=192.168.1.65 -e VARNISH_BACKEND_PORT=80 --name=varnish-alpine thiagofigueiro/varnish-alpine-docker
```

Build image locally:

```bash
git clone git@github.com:thiagofigueiro/varnish-alpine-docker.git
cd varnish-alpine-docker
docker build -t varnish-alpine-docker .
```

## Software
* [Varnish 4.1](https://www.varnish-cache.org/docs/4.1/)
* [Docker Alpine](https://github.com/gliderlabs/docker-alpine)
* [Alpine Linux 3.3](http://www.alpinelinux.org/posts/Alpine-3.3.3-released.html)

## Acknowledgements
* https://github.com/jacksoncage/varnish-docker
