# Webhotel

Script to setup a simple webhotel with Apache, MySQL, PHP, vsFTP, and phpmyadmin.

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

## FTP

Users has access through ftp. VHOST is the username. Password is random generated. Users are not linux users, but separated and stored in /etc/vsftp/passwd

vsFTP is configured to use passive mode, i.d., the server is passive and the client initiates the connection avoiding firewall issues. 

Users has acccess to directories under /srv/www/VHOST/{tmp,htdocs,includes}

## Secure SSH

Consider locking down SSH access to only some specific clients through
/etc/hosts.{allow,deny}

```
./secure_ssh YOUR_IP
```

## Test

```
vagrant up ubuntu
vagrant ssh ubuntu
cd /vagrant
./install
./add foo foo
```
