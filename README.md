# Toybox Reverse Proxy

Running Docker containers SSL dynamic proxy based on the Nginx.

## Requirements

* docker
* docker-compose

## Getting started

### Installation

Download the latest release of toybox-proxy.

```
$ cd /path/to/download
$ git clone https://github.com/nutsllc/toybox-proxy.git
```

### Settings

Copy ``path/to/toybox-proxy/bin/.env.example`` to the same directory as ``.env``.
Edit ``.env`` file.  example below.


```bash
PROXY_HOME=/path/to/toybox-proxy
TOYBOX_UID=1000
TOYBOX_GID=1000

PROXY_CACHE=true
```

### Usage

#### Start Proxy Container
```bash
$ cd tobox-proxy/bin
$ docker-compose up -d
```

It will start three containers. Nginx, docker-gen and letsencrypt-nginx-proxy-companion container.

* Nginx: Proxy Server
* docker-gen: Generate nginx conf files dynamically.
* letsencrypt-nginx-proxy-companion: create and update TLS cirtifications.

## License

* [jwilder/docker-gen](https://github.com/jwilder/docker-gen) - MIT
* [jwilder/docker-letsencrypt-nginx-proxy-companion](https://github.com/jwilder/docker-letsencrypt-nginx-proxy-companion) - MIT
