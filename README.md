# Laptop Setup
This is an Ansible Playbook to get my Ubuntu workstation up and running as quickly as possible. 

## Install
```
sudo apt-get update
sudo apt-get install ansible
ansible-galaxy install -r requirements.yml
ansible-playbook main.yml --ask-become-pass
```

## What this does not do
- Install GPG Keys
- Install SSH Keys

## What this does not Do
- GPG Key Setup
- SSH Key Setup
- Dotfiles (Clone and DL your dotfiles repo)