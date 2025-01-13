# web-gateway-server-ansible
This repository includes a set of ansible roles and a playbook to set up web-server-gateway server

# Prerequisites

- A Server with linux OS (A Debian flavored - ideally an Ubuntu server)
- A host machine to run Ansible scripts remotely with Ansible installed. 
  - Mac OS : `brew install ansible`
  - Other OS : https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu
- If not already installed, install community docker collection for ansible.
  - `ansible-galaxy collection install community.docker`
- Password-less SSH ability to your server. (Using public key authentication)
  - `ssh-copy-id user@server.local` will enable this
- SSH user of the server (e.g : `ubuntu`) is able to password-less `sudo` temporarily.

# How to install

1. Edit `ansible-playbook/inventories/default/group_vars/all.yml` and update the config according to your need.
   - `ansible_user` is the password-less ssh user to the server
2. Edit `ansible-playbook/inventories/default/hosts.ini` and add your server hostname/ip
3. Go into `ansible-playbook` dir and run `./install.sh`




