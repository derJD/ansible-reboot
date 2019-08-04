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
Dependencies
------------

none so far.

Example Playbook
----------------

* basic example:
```
---
- hosts: servers
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
