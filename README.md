
# Traefik stack

This repository is a complete traefik stack able to be deployed in minutes

It uses the following tools to accomplish that:
Ansible
GitHub Actions

There are a few prerequisites before deployment:
1) GitHub secrets for usage

To create GitHub secrets follow this link: <https://docs.github.com/en/actions/security-guides/encrypted-secrets>.

The following secrets are used for deployment:
![secrets](https://user-images.githubusercontent.com/10562868/187651966-85bd7898-1f7d-4fec-9e8e-56567171aa34.PNG)

2) Target Server reachable via ssh over the internet

Make sure that your server is reachable over ssh

3) Ansible - installed on the target server

It is important that Ansible is installed on the target machine. 
Make that sure Ansible has an Ansible.cfg and inventory defined.

The Ansible.cfg and Inventory should be placed in: ./Traefik/Deployments/

The path should be: ./Traefik/Deployments/Ansible.cfg && ./Traefik/Deployments/Inventory


## Installation

Fork this project with GitHub

```bash
  git clone git@github.com:USERNAME/FORKED-PROJECT.git
  cd /path/to/FORKED-PROJECT
```


## Deployment

To deploy this project run

```bash
  git push <REMOTENAME> master 
```

The master branch will trigger the pipeline for deployment.
