# Webhotel

Script to setup a simple webhotel with Apache, MySQL, PHP, and
phpmyadmin.

Tested on Ubuntu 14.04

## Quick Start

Setup the server:

```
./install 
```

Add new vhost and optionally db:

```
./add VHOST [DB]
```

This create directories under /srv/www/VHOST/{tmp,htdocs,includes}

Users has access through ftp. VHOST is the username. Password is
random generated. Users are not linux users, but separated and stored
in /etc/vsftp/passwd

## Test

```
vagrant up ubuntu
vagrant ssh ubuntu
cd /vagrant
./install
./add foo foo
```
