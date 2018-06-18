[![Build Status](https://travis-ci.org/onsentamago/localhost-provision.svg?branch=master)](https://travis-ci.org/onsentamago/localhost-provision)

# localhost-provisioning

Initial setup of Ubuntu18.04 desktop with Ansible.

## Installing Ansible

`````
sudo apt update
sudo apt dist-upgrade -y
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible -y
`````

## Usage

`````
ansible-playbook main.yml
`````
