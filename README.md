Netplan
=========

Configure Netplan.

Role Variables
--------------

| Variable    | Type   | Default      |
| ----------- | ------ | ------------ |
| netplan     | Dict   | ""           |

Example Playbook
----------------

```
- hosts: servers

  vars:
    netplan:
      network:
        version: 2
        ethernets:
          eth1:
            dhcp4: no
            dhcp6: no
            addresses:
            - 192.168.1.14/24
            nameservers:
              addresses:
              - 192.168.1.1
            routes:
            - to: default
              via: 192.168.1.1

  roles:
    - netplan
```

License
-------

MIT

Author Information
------------------

kcir
