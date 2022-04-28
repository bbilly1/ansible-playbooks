# Ansible Playbooks

A collection of Ansible playbooks I use to provision things.

## Ansible VPS setup

Ansible playbook to provision a plain Ubuntu VPS from digitalocean. Expects ssh access for user root. 

- Create user
- Secure ssh
- Configure ufw

### Setup
Copy or rename `vars.samle.yml` to `vars.yml` and set:
- **regular_user**: Default username to create
- **user_password**: Password for new user
- **sshd_port**: Change ssh port

### Run on a single host
```
ansible-playbook -i $hostname, ansible-vps-setup/playbook.yml
```

## Ansible Docker Ubuntu
Ansible playbook to provision an standart Ubuntu LTS server VM. Expects the user *regular_user* to be already created. 

- update and upgrade repo packages
- install basic necessities
- install `docker`
- install `docker compose`
- copy frequently used config files

### Setup
Copy or rename `vars.samle.yml` to `vars.yml` and set:
- **regular_user**: Default username 

### Run on a single host
```
ansible-playbook -i $hostname, -K ansible-docker-ubuntu/playbook.yml
```
