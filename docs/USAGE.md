# Installation

## Single Node Jira Monitoring

This will install the full monitoring stack and with minimal configuration begin monitoring a single node installation of Jira. 

1. Download `atlassian-monitoring-stack-for-jira-full.zip` from the latest release at https://github.com/mminns/Jira-DC-Grafana-Dashboards/releases/
1. Unzip
1. [Configure the JMX Exporter](#Configure-the-JMX-Exporter) to monitor your Jira instance
1. Run the stack
    1. `./start-stack-full.sh`

## Multi-Node Jira Monitoring

This two components allow for a single installation of the reporting stack and an installation per Jira node of the exporting stack.

1. Make a copy `./jmx-exporter/config.yml` for each Jira node, e.g. `./jmx-exporter/{node number}-config.yml`
1. [Configure the JMX Exporter](#Configure-the-JMX-Exporter) to monitor each Jira node using the copied `./jmx-exporter/config.yml` files.
1. Run the exporter stack for each node using the node specific `./jmx-exporter/config.yml` e.g.
    1. `./start-stack-exporter.sh ./jmx-exporter/{node number}-config.yml`


# Configuration

## Configure the JMX Exporter

tbc




