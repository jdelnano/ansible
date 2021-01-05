## Ansible

This repository contains ansible configurations geared at automation related to jOeCHEM

There are roles that were previously used to configure a single server LEMP stack to run jOeCHEM,
but now a single role is used to deploy new versions of the Dockerized jOeCHEM application.

Commands used to deploy to staging + production:
```
# staging
ANSIBLE_CONFIG=./ansible.cfg ansible-playbook -i hosts joechem-docker.yml -t staging_joechem
# production
ANSIBLE_CONFIG=./ansible.cfg ansible-playbook -i hosts joechem-docker.yml -t prod_joechem
```
