# gracc dev environment
Run `docker-compose up -d` to get a full GRACC stack with monitoring running under 
Docker on your local machine.

## Prerequisites
* Recent Docker engine and docker-compose installed

## Services

### Interactive Services
These services expose ports for you to interact with.
* gracc-collector - `http://localhost:8080`
* elasticsearch -  `http://localhost:9200`
* kibana  - `http://localhost:5601`
* grafana  - `http://localhost:3000`
* prometheus  - `http://localhost:9090`
* rabbitmq - `http://localhost:15672`

### Other Services
* gracc-stash-raw
* logspout (collects container logs)
* logstash (sends container logs to elasticsearch)
* cadvisor (collects container telemetry)

### Missing Services
These services are part of the GRACC stack but aren't included yet.
* gracc-request (listens for requests to replay or summarize records)
* gracc-summary (sends requests for record summarization)
