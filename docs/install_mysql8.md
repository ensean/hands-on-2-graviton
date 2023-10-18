## Install MySQL 8 with repo on Amazon Linux 2

`You should consider AWS RDS MySQL as a first choice for DB`

`Please note that MySQL 5.7 on arm is not officially supported by the MySQL team`

* OS: Amazon Linux 2

* Steps to install MySQL 8

1. Setup up repo

```
sudo amazon-linux-extras install epel -y

# the latest version can be found via https://dev.mysql.com/downloads/repo/yum/
sudo yum install https://dev.mysql.com/get/mysql80-community-release-el7-10.noarch.rpm

```

2. Commands to install mysql-server-8

```shell
sudo yum update -y                                  # update repo index
sudo yum install mysql-community-server             # install mysql8 server
sudo systemctl start mysqld                         # start mysql server, you can do some initilization work if you want 
sudo grep 'temporary password' /var/log/mysqld.log  # get the temporary password for root
sudo mysql_secure_installation                      # secure your installation with the temporary password

```

## Install MySQL 8 with repo on Amazon Linux 2023

`You should consider AWS RDS MySQL as a first choice for DB`

`Please note that MySQL 5.7 on arm is not officially supported by the MySQL team`

* OS: Amazon Linux 2023

* Steps to install MySQL 8

1. Setup up repo

```
sudo dnf update

# the latest version can be found via https://dev.mysql.com/downloads/repo/yum/
sudo dnf yum install https://dev.mysql.com/get/mysql80-community-release-el9-4.noarch.rpm



```

2. Commands to install mysql-server-8

```shell
sudo dnf update -y                                  # update repo index
sudo dnf install mysql-community-server             # install mysql8 server
sudo systemctl start mysqld                         # start mysql server, you can do some initilization work if you want 
sudo grep 'temporary password' /var/log/mysqld.log  # get the temporary password for root
sudo mysql_secure_installation                      # secure your installation with the temporary password

```


## Refs

1. https://dev.mysql.com/doc/refman/8.0/en/linux-installation-yum-repo.html
1. https://dev.mysql.com/doc/refman/8.0/en/data-directory-initialization.html


