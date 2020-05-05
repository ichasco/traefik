Traefik
=======

Create Network manualy

```
docker network create traefik
```

Create config

```
cp confs/traefik.toml.example confs/traefik-v1.toml
```

Start Docker-Compose

```
docker-compose --compatibility up -d
```


Labels in containers
--------------------

```
labels:
  - "traefik.enable=true"
  - "traefik.backend=traefik"
  - "traefik.frontend.rule=Host:${URL}"
  - "traefik.port=8443"
```
