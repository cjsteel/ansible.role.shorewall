Role Name
=========

Ansible role for installing and configuring Shorewall

Role Variables
--------------

Required default variable values are located in:

    role/shorewall/defaults/main.yml
    
The values in `role/shorewall/defaults/main.yml` can be easily overridden in the following files:

* project/host_vars/hostname/shorewall/shorewall.yml
* project/group_vars/all/shorewall.yml
* project/group_vars/shorewall.yml

Example Playbook
----------------

project/shorewall.yml

    - hosts: shorewall
      roles:
         - { role: shorewall }

