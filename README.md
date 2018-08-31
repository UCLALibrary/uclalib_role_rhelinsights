uclalib_role_rhelinsights
=========

Ansible role to install the RHEL Insights client and register the system with the Insights service

Requirements
------------

The host must already be attached to a RHEL subscription

Role Variables
--------------

* `insights_packagename` -  defines the name of the Insights package to install via yum

* `insights_clientname` - defines the name of the Insights client to run on the host

* `insights_client_conf_dir` - defines the file system path for the Insights configuration

Dependencies
------------

None.

Example Playbook
----------------

```
---

- name: install_rhel_insights.yml
  become: yes
  become_method: sudo
  hosts: all

  roles:
    - { role: uclalib_role_rhelinsights }
```
