## docker-compose on graviton2

* OS: Amazon Linux 2

* Steps to setup docker-compose

```
sudo -s
export PATH=$PATH:/usr/local/bin
yum -y groupinstall "Development tools" 
yum install -y docker
amazon-linux-extras install -y rust1
yum install -y openssl-devel libffi-devel python3-devel
pip3 install -U pip
pip install docker-compose
docker-compose version
```