# Ansible Wordpress Playbook

Use this ansible playbook to setup a fresh server with the following components:

* Nginx
* Nginx Config for WP Super Cache
* Certbot (Let's Encrypt)
* MySQL
* Memcached
* PHP
* Directories to deploy multiple Wordpress sites
* Swapfile (useful for small DO instances)
* Locales
* Postfix
* Adds users for each vhost
* Tools (tmux, vim, htop, git, wget, curl etc.)

## Prerequisites & Config

1. Rename ```hosts.example``` to ```hosts``` and modify the contents.
2. Rename ```group_vars/all.example``` to ```group_vars/all``` and modify the contentes.

There are a bunch of things you can set in ```group_vars/all```. Don't forget to add your host address to ```hosts```.

## Install Playbook

Run ```ansible-playbook site.yml -i hosts```.
