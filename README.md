create_user
=========

Create a user and upload ssh public key for remote authentications

Requirements
------------

No specific required Ansible
Needs a default ssh public key or a specific key needs to be called out in a variable.

Role Variables
--------------

# Define the user you would like to create
user_name: guest

#Define the user state present or absent
user_state: present

#Define the path to the ssh key
ssh_key: ~/.ssh/id_rsa.pub


Dependencies
------------

None

Example Playbook
----------------

---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: mapr
         user_group: mapr
         ssh_key: ~/.ssh/id_rsa.pub


License
-------

BSD

Author Information
------------------

joseph.fota@hpe.com
