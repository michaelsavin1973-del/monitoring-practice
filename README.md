# Monitoring Practice

Local monitoring with Prometheus, Grafana and Docker Compose.

## Start
Run: docker compose up -d
Check: docker compose ps

## Access
- Prometheus: http://localhost:9090
- Grafana: http://localhost:3000

## Configuration
Prometheus collects metrics from itself and Grafana every 15 seconds.
Grafana's Prometheus data source URL: http://prometheus:9090

## Restore dashboard
Open Grafana → Dashboards → New → Import.
Upload prometheus-monitoring.json.
For a separate copy, change both the name and UID.
Select the Prometheus data source if prompted.
Import and check all five panels.

Dashboard restoration was tested successfully.

## Stop
Run: docker compose down
Data remains in named Docker volumes.
docker compose down -v deletes the volumes and their data.
