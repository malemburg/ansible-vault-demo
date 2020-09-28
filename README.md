Ansible Vault Demo Repository
=============================

This repo is used as demo repository for the Ansible Vault talk at Python Meeting Düsseldorf 2020-09-30.

Configuration
--------------

ansible.cfg
:   Sets the default Ansible parameters

hosts.ini / hosts.yml
:   Hosts inventory; as INI of YAML file

site.yml
:   Playbook

group_vars
:   Group variable files

.vault-password
:   Vault password file (DO NOT COMMIT TO REPO!)

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

    ansible-inventory --list

Edit secret variables:

    ansible-vault edit group_vars/project_secrets.yml

Run playbook:

    ansible-playbook site.yml
