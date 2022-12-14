tinyproxy
=========

[Tinyproxy][1] is a light-weight HTTP/HTTPS proxy daemon for POSIX operating systems.

## dockerhub

```bash
https://hub.docker.com/r/tunnm/tinyproxy
```


## docker-compose.yml

```yaml
version: "3.8"
services:
  tinyproxy:
    container_name: tinyproxy
    image: tunnm/tinyproxy:1.11.1
    ports:
      - "8888:8888"
    volumes:
      - ./data:/etc/tinyproxy
    restart: unless-stopped
```


## Server Setup

```bash
$ docker-compose up -d tinyproxy
```



## Client Setup

```bash
$ curl -x https://127.0.0.1:8888 https://ifconfig.co
```

[1]: https://tinyproxy.github.io/
