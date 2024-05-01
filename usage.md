# Usage Guide for Prometheus and Grafana

This guide will help you understand how to use Prometheus and Grafana for monitoring and visualizing your applications' metrics.

## Querying Data with Prometheus

Prometheus uses PromQL (Prometheus Query Language) to query and manipulate time series data. Here are some common queries you can run:

- **CPU Usage**: `node_cpu_seconds_total{mode="idle"}`
- **Memory Usage**: `node_memory_MemAvailable_bytes`
- **HTTP Requests**: `http_requests_total{method="GET", status="200"}`
- **Latency**: `http_request_duration_seconds{job="my_job"}`

You can run these queries in the Prometheus web interface to retrieve metrics data.

## Creating Dashboards in Grafana

Grafana allows you to create custom dashboards to visualize your metrics data. Here's how to create a basic dashboard:

1. **Add a Panel**: Click on the "Add Panel" button in the Grafana UI.
2. **Choose Visualization**: Select the type of visualization you want to use (e.g., Graph, Singlestat, Table).
3. **Query Data**: Configure the data source (Prometheus) and write your query to retrieve metrics data.
4. **Customize Panel**: Customize the panel settings, including axes, legends, and thresholds.
5. **Repeat**: Repeat the process to add more panels to your dashboard.
6. **Save Dashboard**: Once you're satisfied with your dashboard, click on "Save" to save it.

## Setting Up Alerts

Prometheus allows you to set up alerts based on predefined rules. Here's how to set up an alert:

1. **Define Alerting Rules**: Define alerting rules in the Prometheus configuration file (`prometheus.yml`).
2. **Reload Configuration**: Reload the Prometheus configuration to apply the new alerting rules.
3. **Configure Alertmanager**: Configure the Alertmanager to handle alerts and send notifications (e.g., email, Slack).
4. **Test Alerts**: Test your alerting rules by triggering conditions that would cause an alert to fire.
5. **Monitor Alerts**: Monitor alerts in the Prometheus web interface or the Alertmanager UI.

## Exploring Historical Data

You can use Grafana's Explore feature to interactively query and explore historical data stored in Prometheus. Here's how to use it:

1. **Open Explore**: Click on the "Explore" button in the Grafana UI.
2. **Select Data Source**: Choose the Prometheus data source.
3. **Run Queries**: Write PromQL queries to retrieve historical metrics data.
4. **Visualize Data**: Visualize the queried data using different types of visualizations available in Grafana.

By following these steps, you can effectively use Prometheus and Grafana to monitor your applications and gain insights into their performance and behavior.
