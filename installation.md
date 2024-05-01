# Installation Guide for Prometheus and Grafana

This guide will walk you through the installation process for Prometheus and Grafana on a Linux system. Prometheus is a monitoring and alerting toolkit, and Grafana is a visualization tool that works well with Prometheus.

## Prometheus Installation

### Step 1: Download and Extract Prometheus

```bash
wget https://github.com/prometheus/prometheus/releases/download/{{version}}/prometheus-{{version}}.linux-amd64.tar.gz
tar -xzf prometheus-{{version}}.linux-amd64.tar.gz
cd prometheus-{{version}}.linux-amd64
```

### Step 2: Configure Prometheus

```bash
cp prometheus.yml prometheus.yml.backup
# Edit prometheus.yml to configure targets and other settings
```

### Step 3: Run Prometheus

```bash
./prometheus --config.file=prometheus.yml &
```

### Step 4: Access Prometheus UI

Open your web browser and go to http://localhost:9090 to access the Prometheus web interface.

## Grafana Installation

### Step 1: Add Grafana Repository

```bash
sudo apt-get install -y software-properties-common
sudo add-apt-repository "deb https://packages.grafana.com/oss/deb stable main"
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
sudo apt-get update
```

### Step 2: Install Grafana

```bash
sudo apt-get install -y grafana
```

### Step 3: Start Grafana

```bash
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```

### Step 4: Access Grafana UI
Open your web browser and go to http://localhost:3000 to access the Grafana web interface. The default username and password are usually admin for both.

### Step 5: Add Prometheus Data Source
Log in to the Grafana UI.
Go to Configuration > Data Sources.
Click on "Add data source", select Prometheus, and provide the URL of your Prometheus server (usually http://localhost:9090). Save the configuration.
