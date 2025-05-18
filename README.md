# docker-compose-sidecars

Maintenance and proxy containers to be deployed alongside apps using [cjmay-dev/compose-template](https://github.com/cjmay-dev/compose-template)

## docker-compose.infra.yaml

### stack-back

Automatically detects and backs up all volumes and databases in the docker compose stack (unless explicitly excluded). Supported databases (MySQL, MariaDB, Postgres) are backed up using a stateful SQL dump operation. No configuration is necessary for this to work, but advanced configuration options can be found at [lawndoc/stack-back](https://github.com/lawndoc/stack-back).

### beszel

Remote agent for [beszel](https://github.com/henrygd/beszel), a basic resource monitoring tool with alerting functionality.

### dozzle

Remote agent for [dozzle](https://github.com/amir20/dozzle), a realtime log viewer for containers.

## docker-compose.proxy.yaml

### traefik

A reverse proxy that supports dynamic configuration via container labels.

### cloudflared

Cloudflare's agent used to publish traefik's proxied application to the internet via Cloudflare Tunnel.
