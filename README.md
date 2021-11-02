# dotnet-monitoring
This repo contains Prometheus integration with asp dotnet sample application. 

src.zip file contains a sample asp.net core application

To download prometheus to on-prem environment, use the link below:

https://prometheus.io/download/

Sample prometheus dashboar:

https://grafana.com/grafana/dashboards/159

To download grafana to on-prem on-prem environment, use the link below:

https://grafana.com/grafana/download

To run prometheus locally:

http://localhost:9090/

To run grafan locally:

http://localhost:3000/

Configure prometheus to collect data from a given target, edit prometheus.yml file such as below:

...
# A scrape configuration containing exactly one endpoint to scrape:
# Here it's Prometheus itself.
scrape_configs:
...
  # The job name is added as a label `job=<job_name>` to any timeseries scraped from this config.
  - job_name: 'monitoringapi-2'
    # metrics_path defaults to '/metrics'
    # scheme defaults to 'http'.
    static_configs:
    - targets: ['localhost:8777']
  
    metrics_path: /metrics
...
