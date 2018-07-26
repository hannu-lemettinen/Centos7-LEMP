# Centos7-LEMP
Guide to build LEMP stack in Centos7


## install NGINX and nginx -pagespeed:
### Install ngx_pagespeed dynamic module on CentOS 7

https://www.getpagespeed.com/server-setup/nginx/install-ngx_pagespeed-dynamic-module-centos-7


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
