<!-- This was created with Claude Code -->

shadowman_mattermost_clear_channel
==================================

An Ansible role for shadowman mattermost clear channel.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **mattermost_url**: Variable used in: Get team by name if specified
  - Default: `https://cicd.shadowman.dev:8065`

* **mattermost_team_name**: Variable used in: Get team by name if specified
  - Default: `ansible`

* **town_square_channel**: Variable used in: Get Town Square channel
  - Default: `town-square`

* **posts_per_page**: Variable used in: Get all posts from Town Square channel
  - Default: `200`

* **validate_certs**: SSL/TLS certificate
  - Default: `True`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_mattermost_clear_channel
      vars:
        mattermost_url: <value>
        mattermost_team_name: <value>
        town_square_channel: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
