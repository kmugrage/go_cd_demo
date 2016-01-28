## Getting Started

You can use this setup to start Go with no pipelines or the simple fan-in demonstration that is checked into backup.tar in the root of this repository.

While the server and agent are starting you will see an error in the console showing that the agent is unable to connect to the server. The agent will retry in 1 minute at which point it should be able to connect to the server.

The console will show combined agent and server logging. If you wish to see more specific logging you will need to attach to the running containers individually.

You can browse to the GoCD dashboard at http://DOCKER_HOST_IP:8153

### Get the server running, with no configured pipelines

    > ./bootstrap
    > ./docker-compose up

## Once you have Go running

Run these commands from a different terminal open to the same working directory for the demo. Do not CTRL-C to kill things as it might leave you unable to restart your agent. If you do have trouble restarting the agent, simply remove the agent container.

### [OPTIONAL] Setup a simple fan-in demo

* Navigate to Admin>Config XML
* Click Blue EDIT Button
* Paste contents of config_simple_demo.xml

### Take backup/snapshot (This will stop all services.)

    > ./backup

### stop all containers

    > ./docker-compose stop

### restore from backup/snapshot

    > ./restore
