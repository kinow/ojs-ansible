# OJS playbook

This project contains the automated scripts to set up a OJS server.

## Infrastructure

The infrastructure is comprised of:

* a MySQL database
* nginx
* PHP-fpm
* OJS from a git commit hash

This project includes an Ansible playbook with automated instructions to set up the environment. The playbook
works for Vagrant, but it can also be used locally or to set up a server via SSH.

In order to install the infrastructure you will need:

* Vagrant (and VMWare or VirtualBox), or Docker, a Linux computer or SSH access to a server
* Ansible

## License

Licensed under the MIT License. See LICENSE.txt.
