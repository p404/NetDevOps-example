# NetDevOps Example
Here, you can find an example doing configuration management to JunOS (vSRX) using Ansible.

## Installation steps on Ubuntu 16.04
* Vagrant
    * Install Vagrant
        *   https://www.vagrantup.com/downloads.html
    * Install Virtualbox
        * sudo apt-get install virtualbox
    * JunOS Vagrant pluging install
        * vagrant plugin install vagrant-host-shell
        * vagrant plugin install vagrant-junos

* Ansible
    * Ansible Install
        * sudo apt-get install ansible
        * sudo ansible-galaxy install Juniper.junos
        * sudo pip install git+https://github.com/Juniper/py-junos-eznc.git
 
## Getting up the JunOS lab

    vagrant up

## Available ansible playbooks:

    ansible-playbook -i hosts routers-info.yml
    ansible-playbook -i routers-set-hostname.yml
    ansible-playbook -i routers-shutdown.yml