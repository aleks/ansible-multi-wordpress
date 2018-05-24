# Ansible Multi-vHost/Wordpress Playbook

This Playbook can be used to setup multiple vHosts on a single server. Take a look at `group_vars/all.example` to get an idea of what it does.

## Add vHosts

Each item in `sites_to_set_up` will create:

- An directory where the website data lives: `/var/www/<vhost-name>/www`
- An nginx vhost config (HTTP or HTTPS)
- A user with access to the website directory (chrooted)
- A MySQL database

## Prerequisites & Config

1. Get a fresh Ubuntu 18.04 server
2. Rename ```hosts.example``` to ```hosts``` and modify the contents (Add server IP or hostname.tld).
3. Rename ```group_vars/all.example``` to ```group_vars/all``` and modify the contentes.

## Install Playbook

Run ```ansible-playbook site.yml -i hosts```.

## Roles

- MySQL
- PHP 7.2
- Nginx
- Memcached
- Postfix
- Unattended-Upgrades
- vHosts
- Wordpress (mainly permissions)