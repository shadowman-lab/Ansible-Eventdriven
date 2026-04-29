<!-- This was created with Claude Code -->

shadowman_prometheus
====================

An Ansible role for shadowman prometheus.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **nodeexporter_service_name**: Variable used in: Change Node Exporter State
  - Default: `nodeexporter_{{ inventory_hostname_short }}`

* **prometheus_state**: Variable used in: {{ nodeexporter_service_name }}
  - Default: `started`

* **windows_service_name**: Variable used in: Change Windows Exporter State
  - Default: `Windows Exporter`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_prometheus
      vars:
        nodeexporter_service_name: <value>
        prometheus_state: <value>
        windows_service_name: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
