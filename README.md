[![Build Status](https://travis-ci.org/onsentamago/localhost-provision.svg?branch=master)](https://travis-ci.org/onsentamago/localhost-provision)

# Local Host Provisioning with Ansible

Setup of Ubuntu20.04 desktop with Ansible.

## Pre Install

### set default editor vim

```shell script
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
## Install packages

```shell_script
ansible-playbook main.yml -i hosts --ask-vault-pass
```

## Manually configure settings
- inotify
  - `echo fs.inotify.max_user_watches=524288 | sudo tee /etc/sysctl.d/40-max-user-watches.conf && sudo sysctl --system`
