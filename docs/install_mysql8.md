## Install MySQL 8 with repo 

`You should consider AWS RDS MySQL as a first choice for DB`

`Please note that MySQL 5.7 on arm is not officially supported by the MySQL team`

* OS: Amazon Linux 2

* Steps to install MySQL 8

* Setup up repo, `/etc/yum.repos.d/mysql8.repo`. You can choose the source as your like

```
[mysql-connectors-community]
name=MySQL Connectors Community
baseurl=https://opentuna.cn/mysql/yum/mysql-connectors-community-el7-$basearch/
enabled=1
gpgcheck=1
gpgkey=https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
       https://repo.mysql.com/RPM-GPG-KEY-mysql

[mysql-tools-community]
name=MySQL Tools Community
baseurl=https://opentuna.cn/mysql/yum/mysql-tools-community-el7-$basearch/
enabled=1
gpgcheck=1
gpgkey=https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
       https://repo.mysql.com/RPM-GPG-KEY-mysql


[mysql-8.0-community]
name=MySQL 8.0 Community Server
baseurl=https://opentuna.cn/mysql/yum/mysql-8.0-community-el7-$basearch/
enabled=1
gpgcheck=1
gpgkey=https://repo.mysql.com/RPM-GPG-KEY-mysql-2022
       https://repo.mysql.com/RPM-GPG-KEY-mysql
```

2. Commands to install mysql-server-8

```shell
sudo yum update -y                                  # update repo index
sudo yum install mysql-community-server             # install mysql8 server
sudo systemctl start mysqld                         # start mysql server, you can do some initilization work if you want 
sudo grep 'temporary password' /var/log/mysqld.log  # get the temporary password for root
sudo mysql_secure_installation                      # secure your installation with the temporary password

```

* Refs

1. https://dev.mysql.com/doc/refman/8.0/en/linux-installation-yum-repo.html
1. https://dev.mysql.com/doc/refman/8.0/en/data-directory-initialization.html


