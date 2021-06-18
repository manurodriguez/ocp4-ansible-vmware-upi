cluster roles
=========

This role sets rolebindings for cluster-admins and cluster-readers groups
It also removes kubeadmin secret

Requirements
------------

This role depends on the following roles:
- ldap-oauth
- ldap-group-sync

If groups have not been synced, for the sync
----
oc4 create job sync-now --from=cronjob/cronjob-ldap-group-sync -n <ldap_group_sync_namespace>
----

Role Variables
--------------

Define a group of ldap users to assign the roles,

cluster_reader_group: "ldap-group-to-assign-cluster-reader-role"
cluster_admin_group: "ldap-group-to-assign-cluster-admin-role"

Example Playbook
----------------

Prepare a play with the following:

---
- hosts: localhost
  tasks:
    - include_role:
        name: cluster-roles
---

Then execute: 
----
ansible-playbook roles/cluster-roles/apply/main.yaml
----

License
-------

Apache 2.0

Author Information
------------------

Manuel Rodriguez
