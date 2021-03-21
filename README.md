create_user
===========

Create a user and upload an ssh public key for remote authentication

Requirements
------------

No specific requirement for Ansible.
Need a default ssh public key or a specific key needs to be called out in a variable.

Role Variables
--------------

user_name: default
user_state: present
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

---
- hosts: all
  become: true
  become_user: root
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         #user_state: present
         ssh_key: ~/.ssh/id_rsa.pub

License
-------

MIT

Author Information
------------------

Author: Shanthi Krishnamoorthy
