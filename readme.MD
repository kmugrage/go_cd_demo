# Getting Started

## Requirements

* Docker enabled host
* Reasonable memory and CPU

## First time

    > ./bootstrap
    > ./start

While the server and agent are starting you will see an error in the console showing that the agent is unable to connect to the server. The agent will retry in 1 minute at which point it should be able to connect to the server.

The console will show combined agent and server logging. If you wish to see more specific logging you will need to attach to the running containers individually.

You can browse to the GoCD dashboard at http://DOCKER_HOST_IP:8153

## Subsequent starts

    > ./start

# Once you have GoCD running

Run these commands from a different terminal open to the same working directory for the demo. Do not CTRL-C to kill things as it might leave you unable to restart your agent. If you do have trouble restarting the agent, simply remove the agent container.

## [OPTIONAL] Setup a simple fan-in demo

* Navigate to Admin>Config XML
* Click Blue EDIT Button
* Paste contents of config_simple_demo.xml after the line that begins <server artifactsdir="artifacts"

## Take backup/snapshot (This will stop all services.)

    > ./backup

## stop all containers

    > ./stop

## restore from backup/snapshot

    > ./restore
