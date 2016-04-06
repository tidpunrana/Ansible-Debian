# LEMP Ansible Playbooks

## What is This?

[Ansible playbooks](http://docs.ansible.com/ansible/playbooks.html) for installing LEMP stack (nginx, MySQL, PHP5) on a new [Debian](https://www.debian.org/) server instance.

## How to Use

1. [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html) on your local machine
2. Generate an SSH public key on your local machine: `ssh-keygen`
3. Copy SSH public key to authorized keys file on remote server instance: `~/.ssh/authorized_keys`
4. Update remote server instance address for Ansible to connect to in `cfg/hosts` file
5. Update remote server instance user for Ansible to connect to in `cfg/group_vars/local` file
6. Test that setup is working: `ansible -m ping all`

## Start Install

Once setup has been tested and verified working, start main playbook: `ansible-playbook -s site.yml`

## Further Reading

- [How to Install and Configure Ansible on an Ubuntu 12.04 VPS](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-an-ubuntu-12-04-vps)
- [How To Create Ansible Playbooks to Automate System Configuration on Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-create-ansible-playbooks-to-automate-system-configuration-on-ubuntu)
