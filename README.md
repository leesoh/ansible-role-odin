ODIN
=========

Ansible Galaxy role to install ODIN on all distros.

Requirements
------------

Urlcrazy is no longer under development and spits out an error when running. To fix:

```shell
tlddir=$(locate homophones.rb | sed 's%/[^/]*$%/%')
cd $tlddir
cp tld.rb tld.rb.bak
cat tld.rb | grep '"bd"=>' -v | grep '"bn"=>' -v | grep '"br"=>' -v > tld_tmp.rb
mv tld_tmp.rb tld.rb
```

[Credit](https://github.com/leebaird/discover/issues/40)

Role Variables
--------------

Where will we clone the repo to:

```yml
odin_git_location: '/opt'
```

Optionally, you can provide a backed-up copy of the ODIN keys.config file for upload.

```yml
odin_config_file: ''
```

To pass this parameter on the command line: `ansible-playbook playbook.yml --extra-vars "odin_config_file=keys.config"`. Path is relative to the role folder, not the current folder.

Dependencies
------------

leesoh.git
leesoh.pipenv

Example Playbook
----------------

```yml
- hosts: servers
  roles:
    - leesoh.odin
```

License
-------

BSD-3

Author Information
------------------

ODIN: https://github.com/chrismaddalena/ODIN
