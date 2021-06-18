prepare-bastion
=========

This role downloads the ocp4 binaries and setups the httpd server to host ignition files

Requirements
------------

- Tested on Ansible 2.9 and above
- python3

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
- name: Download OCP4 binaries and prepare Web server
  hosts: bastion
  become: true
  roles:
  - prepare-bastion

  environment:
    http_proxy: "{{ http_proxy }}"
    https_proxy: "{{ https_proxy }}"
    no_proxy: "{{ no_proxy_list }}"
```

Then run:
```
$ ansible-playbook roles/prepare-bastion/apply/main.yaml

```

License
-------

Apache License, Version 2.0

Author Information
------------------

Manuel Rodriguez
