# kickstart

Ansible Playbook to initialize Ubuntu localhost.

## Requirements

* Ubuntu installed (tested on 14.04 LTS)
* sudoer user (put the name as `username` var in `host_vars/localhost.yml`)
    * Recommend passwordless sudoer
    * `git` operations are done via https so key pair is not required.
* Git
    * Required to fetch this repository. Updated to latest via playbook.
* and [Ansible](http://docs.ansible.com/ansible/intro_installation.html)

## Description

Do this:

```shell
$ ansible-playbook -i hosts provision-localhost.yml
```

In the playbook, provisioning is performed on `localhost`. This does not requires SSH at all.

`hosts` file is just a dummy here. Of course you can expand its use beyond `localhost`.

## Vagrant?

Combine this with [Vagrant](https://www.vagrantup.com/) is very nice idea.
