# Laptop Setup
This is an Ansible Playbook to get my Ubuntu workstation up and running as quickly as possible. 

## Install
```
sudo apt-get update
sudo apt-get install ansible
ansible-galaxy install -r requirements.yml
ansible-playbook playbook.yml --ask-become-pass
```

## What this does not do
- Install GPG Keys
- Install SSH Keys
