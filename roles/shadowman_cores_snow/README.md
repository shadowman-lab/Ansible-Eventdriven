<!-- This was created with Claude Code -->

shadowman_cores_snow
====================

An Ansible role for shadowman cores snow.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **datacenter**: Data payload
  - Default: `Default`

* **cluster**: Cluster name or identifier
  - Default: `Default`

* **dec_cores**: Configuration parameter for shadowman_cores_snow
  - Default: `1`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_cores_snow
      vars:
        datacenter: <value>
        cluster: <value>
        dec_cores: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
