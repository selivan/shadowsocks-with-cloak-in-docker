# Shadowsocks with Cloak in docker
Docker compose to create [shadowsocks](https://github.com/shadowsocks) server behind [cloak](https://github.com/cbeuw/Cloak#quick-start) https disguise.
# Usage
```
docker compose build
docker run --rm -it ss-cloak-cloak -key
docker run --rm -it ss-cloak-cloak -uid
# write this values to env.sh
. env.sh
docker compose up -d
```
