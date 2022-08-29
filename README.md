
# Traefik stack

This repository is a complete traefik stack able to be deployed in minutes

It uses the following tools to accomplish that:     
Ansible     
GitHub Actions

There are a few prerequisites before deployment:
1) GitHub secrets for usage
    
    To create GitHub secrets follow this link: https://docs.github.com/en/actions/security-guides/encrypted-secrets

2) Target Server reachable via ssh over the internet

    Make sure that your server is reachable over ssh

3) Ansible - installed on the target server
                            
    It is important that Ansible is installed on the target machine



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

The master branch will trigger the pipeline for Deployment.