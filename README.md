
## Bootstrap
To bootstrap the volumes for the first time do as following:
- `docker-compose up`
- `chown -R 472:1 grafana/`
- `chmod -R 777 grafana/`
- `docker-compose up -d`

### SSH local portforwarding
Instead of exposing ports in docker-compose, we forward their port via SSH to local

To find docker container IP run `docker inspect <container>` and look for _"IPAddress":_

Then, run this on local to do port forwarding in background:
-  `ssh -fNT -L <localport>:<container-ip>:<container-port> <server-ip>`