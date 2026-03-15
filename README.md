# Docker Pi-Hole

## Instalation

1. Configure a macvlan network. e.g.:

```
docker network create -d macvlan \
  --subnet=192.168.20.0/24 \
  --gateway=192.168.20.1 \
  -o parent=eth0.20 \
  pihole_lan_macvlan
``` 

2. Configure `.env` file with your custom settings.

3. Run `docker compose up -d` to start the container.

## Pi-Hole Update

Run `update.sh` to update the pi-hole when necessary. 