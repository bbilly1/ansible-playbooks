# Ansible Playbooks

A collection of Ansible playbooks I use to provision things.

## Ansible Docker Ubuntu
Ansible playbook to provision an standart Ubuntu LTS server VM.

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
