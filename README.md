# Centos7-LEMP
Guide to build LEMP stack in Centos7


## NGINX
### Install ngx_pagespeed dynamic module on CentOS 7

https://www.getpagespeed.com/server-setup/nginx/install-ngx_pagespeed-dynamic-module-centos-7

### NGINX server blocks
https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-on-centos-7


## MariaDB
Install:
```console
sudo yum -y install mariadb-server mariadb
sudo systemctl enable mariadb
```
Start and do secure installation:
```console
sudo systemctl start mariadb
sudo mysql_secure_installation
```

## PHP7.2
https://www.cyberciti.biz/faq/how-to-install-php-7-2-on-centos-7-rhel-7/

install epel-release
```console
sudo yum install epel-release
````

turn on remi release
```console
sudo yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm
```

Install yum-utils packages too:
```console
sudo yum install yum-utils
```

Enable remi repo, run:
```console
sudo yum-config-manager --enable remi-php72
sudo yum update
```
install
```console
yum install php php-fpm php-gd php-json php-mbstring php-mysqlnd php-xml php-xmlrpc php-opcache
```

enable and start php-fpm service
```console
sudo systemctl enable php-fpm.service
sudo systemctl start php-fpm.service
```

## Firewalld
set firewall 

https://www.digitalocean.com/community/tutorials/additional-recommended-steps-for-new-centos-7-servers

```console
sudo yum install firewalld
sudo systemctl start firewalld
sudo firewall-cmd --permanent --add-service=ssh
sudo firewall-cmd --zone=public --permanent --add-service=http
sudo firewall-cmd --zone=public --permanent --add-service=https
```
Reload firewalld to implement the new firewall rules:

```console
sudo firewall-cmd --reload


## Automatic updates
https://linuxaria.com/howto/enabling-automatic-updates-in-centos-7-and-rhel-7

