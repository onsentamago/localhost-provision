[![Build Status](https://travis-ci.org/onsentamago/localhost-provision.svg?branch=master)](https://travis-ci.org/onsentamago/localhost-provision)

# Local Host Provisioning with Ansible

Setup of Ubuntu20.04 desktop with Ansible.

## Pre Install

### set default editor vim

```shell script
sudo apt update
sudo apt install vim -y
sudo update-alternatives --config editor
```

### Be able to sudo without password

```shell script
visudo
```
append this line to the end  
```shell script
%sudo ALL=(ALL) NOPASSWD:ALL
```

## Install Git

```shell script
sudo add-apt-repository ppa:git-core/ppa
sudo apt update
sudo apt install git -y
```

## Install Ansible

```shell script
sudo apt update
sudo apt install ansible -y
```

## Download playbook

```shell script
mkdir dev
cd dev
git clone git@github.com:onsentamago/localhost-provision.git
```

## Install packages

```shell script
cd localhost-provision
ansible-playbook main.yml -i hosts --ask-vault-pass
```

## Manual config
- change keymap
- change DPI
- change CAPS to Ctl

```shell
sudo snap connect mysql-workbench-community:password-manager-service
```