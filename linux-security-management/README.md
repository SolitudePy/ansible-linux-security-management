linux-security-management
=========

This role is intended to manage linux policies for better auditing,monitoring and security.

Role Variables
--------------

Variables are well defined in defaults/main.yml.

parameters:
* auditd_laurel_choice [true/false]
* rsyslog_choice [true/false]
* sudoers_choice [true/false]


Example Playbook
----------------
```yml
- name: Policy Enforcer
  hosts: servers
  gather_facts: true
  ignore_errors: true
  tasks:
    - name: Include Linux Security Management Role
      include_role:
        name: linux-security-management
```
run command: `ansible-playbook <playbook_path> -e "auditd_laurel_choice=false" -e "rsyslog_choice=true" -e "sudoers_choice=true"`

License
-------

BSD

Author Information
------------------

#Cyber
