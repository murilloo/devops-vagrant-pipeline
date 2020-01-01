# devops-vagrant-pipeline
Example pipeline using Vagrant for provisioning a VM and Ansible to install Docker and to create a container on top of it.

## Requirements
- Vagrant >= 2.2.5 (https://www.vagrantup.com/downloads.html)
- Libvirt >= 5.1.0 (https://libvirt.org/sources/)

## Goals
- Run MariaDB on a host with a secret user/password
- Provision a VM
- Linux OS is CentOS7
- MariaDB Version 10.2.14
- Created with mysql user (user: ‘appuser’, pass:’supersecretpassword’)
- Credentials are not readable in the Ansible playbook

## Running
```
$ vagrant up --provider=libvirt
$ vagrant ssh centos (to connect to the VM provisioned)
$ sudo docker ps (to see the containers running)
$ sudo docker exec -it CONTAINER_ID bash (to connect to the container)
```
## Requirements
5
- Vangrant >= 2.2.5
6
- Libvirt >= 5.1.0
