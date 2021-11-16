Ansible Role: Install Docker
================================================================================

An Ansible role that installs Docker.

This role has been tested on:
- Amazon Linux 2
- ArchLinux
- Centos 7 & 8
- Ubuntu 20.04

Variables
----------------------------------------

The variable that you're most likely going to want to change is `docker_users`.
That variable is a list of all the users on the system that should be added to
the `docker` group.
```yml
docker_users: [ admin, docker_admin ]
```

Example Playbook
----------------

```yml
- hosts: k8s-nodes
  roles:
    - {role: install_docker, docker_users: [admin]}
```

License
-------

MIT

Author Information
------------------

This role was created by [shnee](github.com/shnee).
