Ansible Role: AppArmor
=========

This roles installs and enables AppArmor. It will update GRUB default options according to one variable to enable AppArmor at boot.


Role Variables
--------------

The only variable present in this role is used to configure GRUB default options.

Here is an example:

```
grub_default_options="quiet apparmor=1 security=apparmor"
```

The variable above only applies if GRUB does not already contain an option for AppArmor. Therefore, you need to adapt this variable with the options you want.


Dependencies
------------

No dependencies from other roles required.


Example Playbook
----------------

Here is a simple example playbook to use this role:

```
hosts: all
user: myuser
become: true
roles:
  - { role: apparmor, tags: [ 'apparmor' ] }
```

License
-------

MIT / BSD

Author Information
------------------

My name is Gaétan. You can follow me on [Twitter](https://twitter.com/gaetanict)

Website: [ICT Pour Tous](https://www.ictpourtous.com)
