Ansible Role: setup-linux-system
=========

- Install default packages
- Setup timezone and locales

Installation
------------

```shell
$ ansible-galaxy install setup-linux-system
```

To be able to update later and eventually to modify it, prefer using `requirements.yml` with the git source:

```yaml
- name: setup-linux-system
  src: git@github.com:florian-hild/ansible-role-setup-linux-system.git
  scm: git
  version: main
```
And then download it with `ansible-galaxy`:

```shell
$ ansible-galaxy install -r requirements.yml
```

Using `git`, you'll have to be carefull to folder name:

```shell
$ git clone git@github.com:florian-hild/ansible-role-setup-linux-system.git setup-linux-system
```

Role Variables
--------------

Available variables are listed below, along with their default values (see `defaults/main.yml`):

Default:
 ```yaml
package_list_debian:
  - vim
  - curl
  - lsb-release
  - wget
  - sudo
  - git
  - tree
  - rsync
  - net-tools
  - zip
  - unzip

timezone: "Europe/Berlin"
 ```