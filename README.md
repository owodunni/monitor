# README

Instructions on how to setup monitoring of a network with a docker swarm.

## Deploy

```
docker stack deploy --compose-file docker-compose.yml monitoring
```

## Configure

Config files are mounted straight into the docker stack. Edit them and then redeploy the stack to update services.

## Network

We use a swarm network that multiple stack can share. This is so that we can monitor multiple stacks.

```
docker network create --driver=overlay --attachable core
```