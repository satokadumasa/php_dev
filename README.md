# What is eclair
Infra automation for rails, nodejs, mysql, redis, elasticsearch on vagrant using Ansible

# Default Version

- PHP 7.3.12
- MariaDB 5.5.64
- Redis stable
- Elasticsearch 5.6
- Node.js 8.1.2
- Nginx 1.16.1

# To change version
Please edit `roles/*/vars/main.yml`.<br>
But, if with other version works, is not guaranteed.<br>
e.g. may some properties in config file are missing, vice versa.<br>

Regarding OS, more sensitive.<br>
On default using CentOS7.2.<br>
e.g. if you prefer to use Ubuntu, you have to replace `yum` with `apt-get`<br>

# Pre-Setting

 edit `Vagrantfile` as you need.

# How to use

```
$ cd your_directory
$ vagrant up
```

# Destroy and Recreate

```
$ cd your_directory
$ sh reset.sh
```
