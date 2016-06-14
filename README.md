ansible.role.shorewall
======================

[![Build Status](https://travis-ci.org/cjsteel/ansible-role-shorewall.svg?branch=master)](https://travis-ci.org/cjsteel/ansible-role-shorewall)

Ansible role for installing and configuring Shorewall

### Quick Start

#### ssh agent

    exec /usr/bin/ssh-agent $SHELL or eval `ssh-agent -s`
    /usr/bin/ssh-add    

#### Run playbook

    ansible-playbook systems.yml --ask-become-pass

### Role Variables


Required default variable values are located in:

    role/shorewall/defaults/main.yml
    
The values in `role/shorewall/defaults/main.yml` can be easily overridden by placing the vars and new values in one or more of the following locations:

* project/host_vars/pc-001/shorewall/shorewall.yml
* project/group_vars/all/shorewall.yml
* project/group_vars/shorewall.yml

### Playbook Example

#### project/site.yml

This setup allows for the easy addition of roles as well as a lot of control on role parameters.

    ---
    # file: project/site.yml
    - hosts: all
      gather_facts: false
    
    - include: shorewall.yml


#### project/shorewall.yml

    ---
    # file: project/shorewall.yml
    - hosts: shorewall
      roles:
         - { role: shorewall }


