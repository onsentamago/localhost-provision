[![Build Status](https://travis-ci.org/onsentamago/localhost-provision.svg?branch=master)](https://travis-ci.org/onsentamago/localhost-provision)

# localhost-provisioning

Initial setup of Ubuntu18.04 desktop with Ansible.

## Installing Ansible

```shell
sudo apt update
sudo apt dist-upgrade -y
sudo apt-add-repository ppa:ansible/ansible
sudo apt update
sudo apt install ansible -y
```

## Usage

```shell
ansible-playbook main.yml
```

## Manually installed packages
- apt
  - google-cloud-sdk
- linuxbrew
  - doctl
  - youtube-dl
- snap
  - `sudo snap install kubectl --classic`
  - `sudo snap install helm --classic`
  - `sudo snap install android-studio --classic`
- curl or other tools
  - nvm(node version manager)

## Manually configure settings
- inotify
  - `echo fs.inotify.max_user_watches=524288 | sudo tee /etc/sysctl.d/40-max-user-watches.conf && sudo sysctl --system`