# docker_mods
This repository has been deprecated. Please patch and keep images updated yourself.

## ~~`ghcr.io/jtagcat/docker_mods:openssl_ubuntu_latest`~~
Ths image has been deprecated on the basis of reducing depenidencies. Please move the contents directly to your Dockerfile:
```
RUN apt-get update && apt-get install -y \
    openssl ca-certificates \
 && rm -rf /var/lib/apt/lists/*
```

## httpd
Do not use this. The images will be deprecated without further notice.

A higher number includes changes in the lower number.

### ~~`ghcr.io/jtagcat/docker_httpd_mods:01_utf8`~~

Prefers UTF-8 where possible.

[Making the change upstream looks hard™](https://github.com/docker-library/httpd/issues/171), so this image exists.

### ~~`ghcr.io/jtagcat/docker_httpd_mods:02_index.txt`~~

index.txt is used if index.html doesn't exist.

### ~~`ghcr.io/jtagcat/docker_httpd_mods:03_allowoverride`~~

Allows all kinds of `.htaccess` files.
