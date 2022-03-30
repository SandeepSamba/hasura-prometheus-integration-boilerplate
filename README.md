# hasura-prometheus-integration-boilerplate
Boilerplate docker-compose and Prometheus configs to scrape data from Hasura Cloud/Pro Project

### Steps to run
- [Setup](https://hasura.io/docs/latest/graphql/cloud/metrics/integrations/prometheus/) Prometheus Integration for your Project in Hasura cloud. 
- Add the `project id` and `access key` to the `prometheus.yml` file as username and password respectively.
- Run `docker-compose -f docker-compose.yml up -d` to start Prometheus and Grafana.
- Access Grafana dashboard at http://localhost:3000. Login username and password are `admin` and `admin` by default. 
- [Add](https://grafana.com/docs/grafana/latest/datasources/add-a-data-source/) prometheus data source (The URL is http://prometheus:9090)
- [Import](https://grafana.com/docs/grafana/latest/dashboards/export-import/#import-dashboard) the Hasura Metrics Dashboard using the `Hasura Metrics.json` file.
- As we make requests to the Hasura Project, the metrics get updated in the Dashboard.