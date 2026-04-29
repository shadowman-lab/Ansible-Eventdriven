<!-- This was created with Claude Code -->

# Eventdriven Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-Eventdriven)


This directory contains Ansible automation for eventdriven management and operations.

## Overview

The Eventdriven automation provides playbooks and roles for managing and configuring
eventdriven infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [httpd_break](roles/httpd_break/README.md) | Role for httpd break |
| [insights_cve](roles/insights_cve/README.md) | Role for insights cve |
| [insights_delete_remediations](roles/insights_delete_remediations/README.md) | Role for insights delete remediations |
| [servicenow_ticket](roles/servicenow_ticket/README.md) | Role for servicenow ticket |
| [shadowman_cores](roles/shadowman_cores/README.md) | Role for shadowman cores |
| [shadowman_cores_snow](roles/shadowman_cores_snow/README.md) | Role for shadowman cores snow |
| [shadowman_esx_vm_migration_cpu](roles/shadowman_esx_vm_migration_cpu/README.md) | Role for shadowman esx vm migration cpu |
| [shadowman_esx_vm_migration_memory](roles/shadowman_esx_vm_migration_memory/README.md) | Role for shadowman esx vm migration memory |
| [shadowman_mattermost](roles/shadowman_mattermost/README.md) | Role for shadowman mattermost |
| [shadowman_mattermost_clear_channel](roles/shadowman_mattermost_clear_channel/README.md) | Role for shadowman mattermost clear channel |
| [shadowman_mem](roles/shadowman_mem/README.md) | Role for shadowman mem |
| [shadowman_passwd](roles/shadowman_passwd/README.md) | Role for shadowman passwd |
| [shadowman_prometheus](roles/shadowman_prometheus/README.md) | Role for shadowman prometheus |
| [shadowman_selinux](roles/shadowman_selinux/README.md) | Role for shadowman selinux |
| [shadowman_sudoers](roles/shadowman_sudoers/README.md) | Role for shadowman sudoers |
| [shadowman_systemd_create](roles/shadowman_systemd_create/README.md) | Role for shadowman systemd create |
| [shadowman_systemd_remove](roles/shadowman_systemd_remove/README.md) | Role for shadowman systemd remove |
| [shadowman_win_firewall](roles/shadowman_win_firewall/README.md) | Role for shadowman win firewall |
| [trigger_high_cpu](roles/trigger_high_cpu/README.md) | Role for trigger high cpu |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| EDAInsightsCVE.yml | Playbook for EDAInsightsCVE | {{ insights_adv_target_host }} |
| EDAInsightsMalware.yml | Playbook for EDAInsightsMalware | localhost, localhost |
| EDANodeExporter.yml | Playbook for EDANodeExporter | {{ vm_name }}, localhost, {{ vm_name }} |
| EDASELinuxDisabled.yml | Playbook for EDASELinuxDisabled | {{ vm_name }}, localhost, {{ vm_name }} |
| EDAwindowsfirewall.yml | Playbook for EDAwindowsfirewall | {{ vm_name | default('all')}} |
| InsightsRemediationDelete.yml | Playbook for InsightsRemediationDelete | localhost |
| alertmanager.yml | Playbook for alertmanager | all |
| edaserverexporter.yml | Playbook for edaserverexporter | all |
| gitops_on_pr.yml | Playbook for gitops on pr | localhost |
| gitops_on_push.yml | Playbook for gitops on push | localhost |
| httpd_break.yml | Playbook for httpd break | {{ host_to_break }} |
| mattermost.yml | Playbook for mattermost | localhost |
| mattermost_channel_clear.yml | Playbook for mattermost channel clear | localhost |
| nodeexporter_restart.yml | Playbook for nodeexporter restart | {{ vm_name | default('localhost') }} |
| nodeexporter_stop.yml | Playbook for nodeexporter stop | {{ vm_name | default('localhost') }} |
| passwd_restore.yml | Playbook for passwd restore | all |
| sudoers_restore.yml | Playbook for sudoers restore | all |
| systemd_remove.yml | Playbook for systemd remove | all |
| systemd_setup.yml | Playbook for systemd setup | all |
| trigger_high_cpu.yml | Playbook for trigger high cpu | {{ high_cpu_host }} |
| vm_cores decrease.yml | Playbook for vm cores decrease | {{ vm_name | default('localhost') }} |
| vm_cores increase.yml | Playbook for vm cores increase | {{ vm_name | default('localhost') }} |
| vm_cores increase servicenow.yml | Playbook for vm cores increase servicenow | {{ vm_name | default('localhost') }} |
| vm_cores restore.yml | Playbook for vm cores restore | {{ vm_name | default('localhost') }} |
| vm_mem decrease.yml | Playbook for vm mem decrease | {{ vm_name | default('localhost') }} |
| vm_mem increase.yml | Playbook for vm mem increase | {{ vm_name | default('localhost') }} |
| vm_mem restore.yml | Playbook for vm mem restore | {{ vm_name | default('localhost') }} |
| vmwarehostcpumigration.yml | Playbook for vmwarehostcpumigration | localhost |
| vmwarehostmemmigration.yml | Playbook for vmwarehostmemmigration | localhost |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run EDAInsightsCVE.yml

# Run in stdout mode
ansible-navigator run EDAInsightsCVE.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - insights_cve
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-Eventdriven/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
