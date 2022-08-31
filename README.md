
# Traefik stack

This repository is a complete traefik stack able to be deployed in minutes

It uses the following tools to accomplish that:
Ansible, 
GitHub Actions

There are a few prerequisites before deployment.

## Prerequisites

1 - GitHub secrets for usage

To create GitHub secrets follow this link: <https://docs.github.com/en/actions/security-guides/encrypted-secrets>.

The following secrets are used for deployment:
![secrets](https://user-images.githubusercontent.com/10562868/187651966-85bd7898-1f7d-4fec-9e8e-56567171aa34.PNG)

2 - Target Server reachable via ssh over the internet

3 - Ansible - installed on the target server

It is important that Ansible is installed on the target machine. 
Also make sure that Ansible has an Ansible.cfg and inventory defined in the same folder as de deployment script.

The Ansible.cfg and Inventory should be placed in: ./traefik/Deployments/

The path should be: ./traefik/Deployments/Ansible.cfg && ./traefik/Deployments/Inventory


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

The master branch will trigger the pipeline for deployment. Or you can dispatch the workflow by going to:

## On the forked repo homepage
![page 1](https://user-images.githubusercontent.com/10562868/187653581-856d24f2-590b-4569-9fbc-8b3aca4d5b1c.PNG)

## Navigate to the Actions page
![page 2](https://user-images.githubusercontent.com/10562868/187653836-2e1ff70b-df94-461a-b40c-6e1eff537ccd.PNG)

## Trigger Deployment
Select the work flow you want to trigger and press the blue underscored button (The deployment is the only file that has a workflow_dispatch)
![page 3](https://user-images.githubusercontent.com/10562868/187654844-c20de884-21b2-4df1-86a6-a2a221497483.PNG)
