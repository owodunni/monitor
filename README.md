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

## Node exporter

To export machine metrics we use [node-exporter](https://github.com/prometheus/node_exporter)

```
sudo apt install prometheus-node-exporter
```

Check that the service is running:
```
sudo service prometheus-node-exporter status
```
