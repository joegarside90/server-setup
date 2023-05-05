# Laptop Setup
This is an Ansible Playbook to get my Debian workstation up and running as quickly as possible. 


## Prereqs
As your created user will not have sudo access its probably worth adding your user to the sudo group and restarting
```
su -
usermod -aG sam
```

Once you've downloaded the repo uncomment the roles you want. e.g. Work for Work Machines. Note if your distro has just released some third party repositories may not be supported yet like Hashicorp and Docker

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
- Install VS Codes Plugins (This is handled by the sync in VS Code when you log in)

## Known bugs
- The 1Password install (May need to comment/uncomment stuff for the time being until a better solution is sorted)