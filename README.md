# README

Instructions on how to setup monitoring of a network with a docker swarm.

## Deploy

```
docker stack deploy --compose-file docker-compose.yml monitor
```

## Configure

Config files are mounted straight into the docker stack. Editing them and then go to portainer to update the service.
Don't re deploy the stack because that will flush persistent storage..