Self Provisioner
=========

This template allows to remove self provisioner rolebinding from normal users

Requirements
------------

Role Variables
--------------

Example Playbook
----------------

Prepare a play with the following:

---
- hosts: localhost
  tasks:
    - include_role:
        name: self-provisioner
---

Then execute: 
----
ansible-playbook roles/self-provisioner/apply/main.yaml
----

License
-------

Apache 2.0

Author Information
------------------

Manuel Rodriguez
