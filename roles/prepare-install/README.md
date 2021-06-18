prepare-install
=========

This role generates the install-config.yaml and manifests to deploy Red Hat Openshift

Requirements
------------

- Tested on Ansible 2.9 and above
- python3, python-pip3, and python3-netaddr

Role Variables
--------------

See defaults/main.yaml for full details of the role variables


Dependencies
------------

This role has no dependencies

Example Playbook
----------------

```
---
- name: UPI on Vsphere Playbook
  hosts: localhost
  roles:
  - prepare-install

```

Then run:
```
$ ansible-playbook roles/prepare-install/apply/main.yaml

```

License
-------

Apache License, Version 2.0

Author Information
------------------

Manuel Rodriguez
