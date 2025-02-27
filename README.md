# Server Setup
Ansible Playbook to setup and configure the Intel N100 server running Rocky Linux


## Prereqs
Your created user will not have sudo access. If so its probably worth adding your user to the sudo group and restarting
```
su -
usermod -aG sudo sam
```

Once you've downloaded the repo
```
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install git -y
git clone https://github.com/sbt92/laptop-setup
```

Uncomment the roles you want. e.g. Work for Work Machines. Note if your distro has just released some third party repositories may not be supported yet like Hashicorp and Docker

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