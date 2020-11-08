# bootstrap-ubuntu
Playbook for keeping track of my Laptop/PC Ubuntu Configuration

This is WIP as I don't recall every step I made in the past for my current setup (manual work, buuh).  
As I introduce new config changes to my systems, they will be added here.

Also, should I set up one of my systems completely from scratch in the future, I will put every step here in this playbook.

Plz remember future me.

**UPDATE: Ok, I remembered and now everything is included in this playbook.** :grin:

As baseline, Ubuntu (20.10) is installed in "Minimal Install" mode.


### Instructions
On a fresh installation, install Ansible and git:
```
sudo apt install ansible git
```

Clone the git repo:
```
git clone https://github.com/shaderecker/bootstrap-ubuntu.git
```

Then run the Playbook for the first time:
```
ansible-playbook bootstrap.yaml --ask-become-pass
```

Afterwards you can remove the Ansible apt package as it is managed via pip now:
```
sudo apt remove ansible
```

For consecutive runs, you can just use this, as the sudo password is no longer required:
```
ansible-playbook bootstrap.yaml
```
