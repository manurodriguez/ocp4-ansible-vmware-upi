prepare-install
=========

This role generates the install-config.yaml and manifests to deploy Red Hat Openshift

Requirements
------------

- Tested on Ansible 2.9 and above
- python3, python-pip3, and python3-netaddr

Role Variables
--------------

See inventory/hosts for full details of the role variables


Dependencies
------------

This role has no dependecines

Example Playbook
----------------

File: generate-config.yml
```
---
- name: UPI on Vsphere Playbook
  hosts: localhost
  roles:
  - prepare-install

  environment:
    http_proxy: "{{ http_proxy }}"
    https_proxy: "{{ https_proxy }}"
    no_proxy: "{{ no_proxy_list }}"
```

Then run:
```
$ ansible-playbook prepare-install.yml

```

License
-------

Apache License, Version 2.0

Author Information
------------------

Manuel Rodriguez
