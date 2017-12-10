# docker-volume-netshare in container

How to run: look at [docker-compose.yml](docker-compose.yml)

```
docker-volume-netshare:
  image: ephillipe/docker-volume-netshare:latest
  command: efs
  net: host
  privileged: true
  restart: always
  volumes:
  - /run:/run
  - /var/run:/var/run:rw
  - /dev:/host/dev:rw
  - /run/docker/plugins:/run/docker/plugins:rw
  - /var/lib/docker-volumes/netshare:/var/lib/docker-volumes/netshare:shared
```
