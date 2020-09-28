Ansible Vault Demo Repository
=============================

This repo is used as demo repository for the Ansible Vault talk
at Python Meeting Düsseldorf 2020-09-30.

Installation
------------

Run

    make install

Then test with

    ansible demo-host -m ping

Note: You may have to edit the configuration files to match your setup.

Commands
--------

List host inventory:

    ansible-inventory --ask-vault-password --list

Edit secret variables:

    ansible-vault edit group_vars/project_secrets.yml

Run playbook:

    ansible-playbook --ask-vault-password site.yml
