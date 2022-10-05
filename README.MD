# Ansible Network Stack

This repository is a Ansible network stack able to be deployed in minutes.

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

Also make sure that your forked repo has the right inventory secrets defined. 
If not, the intergrate.yml pipeline can't run on the target server(s)
![inventory](https://user-images.githubusercontent.com/10562868/187670468-34125a16-e593-4c2c-92d8-3507b310e033.PNG)

The deployment.yml can be found under: ./FORKED REPO/.github/workflows

## Usage

To run the ansible scripts locally, make sure you're in the right folder to run the script.

For example when you need to probe a Switch, make sure you're in the "network_probe folder".
Use the following command to run the ansible playbook: ansible-playbook probe_vlan.yml

To run the script from Github Actions, make sure the Ansible script can be communicate with the network else it will fail.