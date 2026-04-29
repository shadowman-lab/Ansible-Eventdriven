<!-- This was created with Claude Code -->

shadowman_selinux
=================

An Ansible role for shadowman selinux.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **selinux_policy**: Variable used in: Change SELinux State
  - Default: `targeted`

* **selinux_state**: Variable used in: Change SELinux State
  - Default: `enforcing`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: shadowman_selinux
      vars:
        selinux_policy: <value>
        selinux_state: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
