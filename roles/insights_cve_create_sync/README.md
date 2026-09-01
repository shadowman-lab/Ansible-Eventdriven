<!-- This was created with Claude Code -->

insights_cve
============

An Ansible role for insights cve.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **mattermost_url**: Variable used in: Send notification message via Mattermost on CVE Issue
  - Default: `https://cicd.shadowman.dev:8065`

* **insights_api_url**: Variable used in: Create a list of advisories
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
    - role: insights_cve
      vars:
        mattermost_url: <value>
        insights_api_url: <value>
        sso_endpoint: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
