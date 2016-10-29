# OJS Server (Vagrant)

This is the documentation for the OJS infrastructure, using Vagrant and VirtualBox/VMWare to
create the infrastructure for the server side.

## Requirements

In order to have a similar infrastructure running locally, you will need the following tools:

* Vagrant
* VirtualBox or VMWare
* Ansible

If you are using Ubuntu, you can install these with `sudo apt-get install -y vagrant virtualbox ansible`

You will need at least 1GB of memory, 1 core and between 10 and 20 GB for the Virtual Machine.

## Installation

Vagrant will create a Ubuntu Trusty Virtual Machine using VirtualBox/VMWare, and will provision it
using Ansible. If you want to re-run some of the tasks of the Ansible playbook, you can use tags (see
ansible-vagrant.sh script).

The virtual machine will be running Nginx listening to the guest port 80. The 80 port of the virtual machine is exposed
to the host machine as 8000. The MySQL port will be exposed as 3307.

You can mirror local ports with SSH.

`sudo ssh -p 2222 -gNfL 80:localhost:80 vagrant@localhost -i .vagrant/machines/default/virtualbox/private_key`

Where 2222 is the default port used by Vagrant.

## Testing

You can test OJS opening the following URL in your browser.

http://localhost:8000
