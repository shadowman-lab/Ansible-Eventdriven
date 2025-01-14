# Ansible-Eventdriven
[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Eventdriven)

Code to provide event driven automation

Currently supports RHV and VMWare for:
Increasing/Decreasing CPU cores
Increasing/Decreasing Memory
Starting Node Exporter (Prometheus)

Automated Response to Red Hat Insights CVEs

ServiceNow Ticket Creation and chat notification (Mattermost)

VMWare VM Host migration to ESX host

Automated response using Systemd for local user creation or sudoers file changes

Can use any monitoring/alerting service into Ansible Tower API
