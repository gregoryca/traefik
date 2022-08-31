
# Traefik stack

This repository is a complete traefik stack able to be deployed in minutes

It uses the following tools to accomplish that:
Ansible, 
GitHub Actions

There are a few prerequisites before deployment.

## Prerequisites

1 - GitHub secrets for usage

To create GitHub secrets follow this link: <https://docs.github.com/en/actions/security-guides/encrypted-secrets>

The following secrets are used for deployment:
![secrets](https://user-images.githubusercontent.com/10562868/187651966-85bd7898-1f7d-4fec-9e8e-56567171aa34.PNG)

2 - Target server(s) reachable via ssh over the internet

3 - Ansible installed on the target server(s)

It is important that Ansible is installed on the target machine. 

Also make sure that your forked repo has the right inventory secrets defined. 
If not, the intergrate.yml pipeline can't run on the target server(s)
![inventory](https://user-images.githubusercontent.com/10562868/187670468-34125a16-e593-4c2c-92d8-3507b310e033.PNG)

The intergrate.yml can be found under: ./FORKED REPO/.github/workflows

Feel free to add, or change the ansible deployment script according to your needs.
Do not forget to change the traefik URL in the docker-compose file, to a C-NAME record which points to your home address using DynDNS (DDNS)

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
Select the work flow you want to trigger and press the blue underscored button.
![page 3](https://user-images.githubusercontent.com/10562868/187654844-c20de884-21b2-4df1-86a6-a2a221497483.PNG)