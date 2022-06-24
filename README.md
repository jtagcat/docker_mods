# docker_mods

## ~~`ghcr.io/jtagcat/docker_mods:openssl_ubuntu_latest`~~
Do not use this. You don't need an additional (security) dependency.

Use `debian:stable-slim` with the following command in your Dockerfile:
```
RUN apt-get update && apt-get install -y \
    openssl ca-certificates \
 && rm -rf /var/lib/apt/lists/*
```

## httpd
Again, try not to use this. I will try to phase this image out as well.

A higher number includes changes in the lower number.

Defining the files in the repo is more clear. Generating and making images out of patchfiles gets messy. [xkcd:1205](https://xkcd.com/1205)

### `ghcr.io/jtagcat/docker_httpd_mods:01_utf8`

Prefers UTF-8 where possible.

[Making the change upstream looks hard™](https://github.com/docker-library/httpd/issues/171), so this image exists.

### `ghcr.io/jtagcat/docker_httpd_mods:02_index.txt`

index.txt is used if index.html doesn't exist.

### `ghcr.io/jtagcat/docker_httpd_mods:03_allowoverride`

Allows all kinds of `.htaccess` files.
