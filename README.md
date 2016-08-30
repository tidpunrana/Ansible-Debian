# Ansible Playbooks - LEMP Stack

By Josh Lapham [josh@joshlapham.com]

License: [Beerware](https://en.wikipedia.org/wiki/Beerware)

## What This Is

[Ansible playbooks](http://docs.ansible.com/ansible/playbooks.html) for provisioning a new [Debian](https://www.debian.org/) server instance with LEMP stack (nginx, MySQL, PHP5).

Working with [Debian 8 "Jessie"](https://wiki.debian.org/DebianJessie).

## How to Use

1. [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html) on your local machine
2. Generate an SSH public key on your local machine: `ssh-keygen`
3. Copy SSH public key to authorized keys file on remote server instance: `~/.ssh/authorized_keys`
4. Update `config/staging` file with correct username and host
5. Test that setup is working: `ansible -m ping all`

### Start Provisioning

Once setup has been tested and verified working, start main playbook:

`ansible-playbook -s provision.yml -i config/staging`
