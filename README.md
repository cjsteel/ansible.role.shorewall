Role Name
=========

Ansible role for installing and configuring Shorewall

Role Variables
--------------

Required default variable values are located in:

    role/shorewall/defaults/main.yml

Additional examples are here:

    role/shorewall/files/shorewall*
    
The values in `role/shorewall/defaults/main.yml` can be overridden in the following places:

* project/host_vars/hostname/shorewall.yml  see files/shorewall.yml example
* project/group_vars/all/shorewall.yml      see files/shorewall.yml example
* project/group_vars/shorewall.yml

Defining vars in vars/main.yml overides vars in all of the above locations.

* `role/shorewall/vars/main.yml`

Example Playbook
----------------

project/shorewall.yml

    - hosts: shorewall
      roles:
         - { role: shorewall }

