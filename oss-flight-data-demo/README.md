# OSS Flight Data Demo

## Quick start

1. Run `docker compose --profile default up -d`.       

2. Ingest data into [Druid](https://localhost:8888) from adsb-json topic with the spec in ../druid/ingestion_spec.json. Credentials are available from DevRel.

3. After all messages have been ingested you can check out visualisations in [Grafana](localhost:3000) on port 3000, username and password for Grafana are both `druid`.

## TODO

* Use Flink to (or otherwise) consolidate/filter records for aircraft to reduce the number of null longitudes, latitudes, and altitudes
* Alternatively, can this be achieved with rollup? Rollup on 1 second time intervals and take the average  longitudes, latitudes, and altitudes?
* Deploy using Minikube instead of docker? (with a view to rolling this out to learn Druid)
