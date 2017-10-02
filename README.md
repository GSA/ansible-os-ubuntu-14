<<<<<<< HEAD
# ansible-os-ubuntu-14
[![CircleCI](https://circleci.com/gh/GSA/ansible-os-ubuntu-14.svg?style=svg)](https://circleci.com/gh/GSA/ansible-os-ubuntu-14)
Ansible Roles for Ubuntu 14
=======
>>>>>>> ubuntu_ansible_dev


Ubuntu 14 GSA Benchmark
====================

## This role is still under development

This ansible content will configure Ubuntu 14 machine to be GSA compliant.

This role **will make changes to the system** that could break things. This is not an auditing tool but rather a remediation tool to be used after an audit has been conducted. For compliance auditing, use a tool such as [nessus](https://www.tenable.com/products/nessus-vulnerability-scanner) or [CIS-CAT](https://learn.cisecurity.org/cis-cat-landing-page)

## IMPORTANT INSTALL STEP

This code is based on the GSA Ubuntu 14 v1.0 and the [CIS Ubuntu 14 Benchmark v2.0.0 ](https://community.cisecurity.org/collab/public/index.php).

Requirements
------------

You should carefully read through the tasks to make sure these changes will not break your systems before running this playbook.

Role Variables
--------------
There are many role variables defined in defaults/main.yml.

By default, many of the variables are turned off. Please review and adjust to meet your organizational requirements.

Note, a subset of controls were removed due to operational impact or organizational dependent variables. Those are listed [here](https://docs.google.com/spreadsheets/d/1KpIFcgn8a_FMATd3Rphm0M9d7FBeJf6VvyIRBgenTEQ/edit#gid=0) *Note: Must have a GSA account to access.


Dependencies
------------

Ansible > 1.9

Example Playbook
-------------------------

```
---
- name: Harden Server
  hosts: all
  become: yes

  roles:
    - gsa_hardening
```
How to test locally
--------------------------
```
ansible-playbook playbook.yml --connection=local
```

License
-------

Apache
