project-template
=========

This template allows to setup the default config for all templates

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
        name: project-template
---

Then execute: 
----
ansible-playbook roles/project-template/apply/main.yaml
----

License
-------

Apache 2.0

Author Information
------------------

Manuel Rodriguez
