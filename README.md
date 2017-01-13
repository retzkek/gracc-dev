# gracc dev environment
Run `docker-compose up -d` to get a full GRACC stack with monitoring running under 
Docker on your local machine. Go to localhost:8888 to view service frontend.

Run `docker-compose -f docker-compose.probes.yaml up` to run test probes.

## Prerequisites
* Recent Docker engine and docker-compose installed

## Services

### Core Services
* elasticsearch
* rabbitmq
* gracc-collector
* gracc-stash-raw

### Monitoring Frontend Services
* kibana
* grafana
* prometheus
* nginx (listens on `localhost:8888`, proxies other services)

### Other Services
* logspout (collects container logs)
* logstash (sends container logs to elasticsearch)
* cadvisor (collects container telemetry)

### Missing Services
These services are part of the GRACC stack but aren't included yet.
* gracc-request (listens for requests to replay or summarize records)
* gracc-summary (sends requests for record summarization)
