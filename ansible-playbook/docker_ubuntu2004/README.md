# Docker on Ubuntu 20.04

This playbook will install Docker an Ubuntu 20.04 machine
A number of containers will be created with the options specified in the `vars/default.yml` variable file.

## Settings

- `create_containers`: number of containers to create.
- `default_container_name`: default name for new containers.
- `default_container_image`: default image for new containers.


## Running this Playbook

Quick Steps:

### 1. Obtain the playbook
```shell
git clone https://github.com/tyao117/
cd ansible-playbooks/docker_ubuntu2004
```

### 2. Customize Options

```shell
nano vars/default.yml
```

```yml
#vars/default.yml
---
create_containers: 4
default_container_name: docker
default_container_image: ubuntu
```

### 3. Run the Playbook

```command
ansible-playbook -l [target] -i [inventory file] -u [remote user] playbook.yml
ansible-playbook -i ../hosts playbook.yml
```

For more information on how to run this Ansible setup, please check this guide: [How to Use Ansible to Install and Set Up Docker on Ubuntu 18.04](https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-install-and-set-up-docker-on-ubuntu-18-04).
