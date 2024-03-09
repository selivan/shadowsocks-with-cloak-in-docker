# Shadowsocks with Cloak in docker
Docker compose to create [shadowsocks](https://github.com/shadowsocks) server behind [cloak](https://github.com/cbeuw/Cloak#quick-start) https disguise.
# Usage
```
docker compose build
docker run --rm -it ss-cloak-cloak -key
docker run --rm -it ss-cloak-cloak -uid
docker rmi ss-cloak-cloak # this image had default password values
# write generated key and uid to docker-compose.env
docker compose --env-file=docker-compose.env up -d
```
