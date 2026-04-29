<!-- This was created with Claude Code -->

insights_delete_remediations
============================

An Ansible role for insights delete remediations.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **insights_api_url**: Variable used in: Create a list of Remediations
  - Default: `https://console.redhat.com/api`

* **sso_endpoint**: Variable used in: Get Token from Service Account
  - Default: `https://sso.redhat.com/auth/realms/redhat-external/protocol/openid-connect/token`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: insights_delete_remediations
      vars:
        insights_api_url: <value>
        sso_endpoint: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
