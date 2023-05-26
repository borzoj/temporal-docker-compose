# Temporal server Docker setup with monitoring tools

Based on https://github.com/temporalio/docker-compose

## Prerequisites

To use these files, you must first have the following installed:

- [Docker](https://docs.docker.com/engine/installation/)
- [docker-compose](https://docs.docker.com/compose/install/)

## How to use

The following steps will run a local instance of the Temporal Server using the default configuration file (`docker-compose.yml`):

1. Clone this repository.
2. Change directory into the root of the project.
3. Run the `docker-compose up` command.

```bash
git clone git@github.com:borzoj/temporal-docker-compose.git
cd  temporal-docker-compose
docker-compose up
```

## Available URLs

- Temporal Server: [http://localhost:8080](http://localhost:8080)
- Prometheus [http://localhost:9090](http://localhost:9090)
- Grafana [http://localhost:8085](http://localhost:8085)

## Server and worker monitoring

Prometheus is configured to scrape server and worker metrics. This project only provides the server. It's meant to be used in conjunction with a worker provided in [https://github.com/borzoj/temporal-hello-world](https://github.com/borzoj/temporal-hello-world)

## Grafana Dashboard

A Grafana dashboard with basic Temporal workflow metrics is provided in `grafana/dashboards/temporal.json`. You can [import it directly into Grafana](https://grafana.com/docs/grafana/latest/dashboards/manage-dashboards/#export-and-import-dashboards). This dashboard uses worker metrics.


