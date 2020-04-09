reboot
=========

Reboot node if necessary.

Requirements
------------

none so far.

Role Variables
--------------


| Variable | Type | Default | Description |
| -------- | ---- | ------- | ----------- |
| `reboot_test_command` | String | `whoami` | Command to check if node is ready after being reachable again. |
| `reboot_uptime_days` | Number | None | If this is set, debian nodes with higher uptime than this value will be rebooted |
Dependencies
------------

none so far.

Example Playbook
----------------

* basic example:
```
---
- hosts: servers
  vars:
    reboot_uptime_days: 30
  tasks:
    - package: upgrade=full update_cache=yes
    - include_role: name=derJD.reboot
```

License
-------

BSD

Author Information
------------------

[derJD](https://github.com/derJD/)
