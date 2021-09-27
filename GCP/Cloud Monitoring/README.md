


# GCP: Cloud Monitoring: Qwik Start

###  Create a Monitoring workspace
* Navigation **menu > Monitoring**
## Install the Monitoring and Logging agents

### Install agents on the VM

1. Run the Monitoring agent install script command in the SSH terminal of your VM instance to install the Cloud Monitoring agent.
```
curl -sSO https://dl.google.com/cloudagents/add-monitoring-agent-repo.sh
sudo bash add-monitoring-agent-repo.sh

sudo apt-get update

sudo apt-get install stackdriver-agent
```

When asked if you want to continue, enter Y.

2 Run the Logging agent install script command in the SSH terminal of your VM instance to install the Cloud Logging agent

```
curl -sSO https://dl.google.com/cloudagents/add-logging-agent-repo.sh
sudo bash add-logging-agent-repo.sh

sudo apt-get update

sudo apt-get install google-fluentd
```

## Create an uptime check
## Create an alerting policy
