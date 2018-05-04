ODIN
=========

Ansible role to install ODIN on all distros.

Requirements
------------

None

Role Variables
--------------

odin_git_location: '/opt'

Dependencies
------------

leesoh.git

Example Playbook
----------------

- hosts: servers
  roles:
    - { role: leesoh.odin }

License
-------

BSD3

Author Information
------------------

ODIN: https://github.com/chrismaddalena/ODIN
