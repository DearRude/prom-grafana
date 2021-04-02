
## Run
Just run with docker-compose:
- `docker-compose up`

### SSH local portforwarding
Instead of exposing ports in docker-compose, you acn forward their port via SSH to local

To find docker container IP run `docker inspect <container>` and look for _"IPAddress":_

Then, run this on local to do port forwarding in background:
-  `ssh -fNT -L <localport>:<container-ip>:<container-port> <server-ip>`
