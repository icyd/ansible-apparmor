Ansible-apparmor
=========

Ansible role to install Apparmor.

Take into consideration this role do not install other profiles other than the ones provided by the listed packages and will convert all the existing profiles  to **complain** mode, so is your responsibility to create and enforce them.

Also take into consideration to make apparmor available, a reboot of the machine is required, by default this role wont reboot unless is specified with the variables available.

Requirements
------------

**Role tested only on:**
    - Debian 9.

Role Variables
--------------

`apparmor_allow_reboot` is by default `false`, to allow the reboot of the host machine, set it to `true`.

Installation
------------

Change directory to the _role_ directory of your playbook and run:

```bash
git clone https://github.com/icyd/rkhunter-ansible-role
```

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - role: ansible-apparmor
```


License
-------

GLPv2
