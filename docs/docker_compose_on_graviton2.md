## docker-compose on graviton2

* OS: Amazon Linux 2

* Steps to setup docker-compose

1. Install docker

```
sudo yum update -y

sudo amazon-linux-extras install -y docker
sudo service docker start
sudo usermod -a -G docker ec2-user
docker info

```
2. 安装docker-compose
```
sudo -s
export PATH=$PATH:/usr/local/bin
yum -y groupinstall "Development tools" 
amazon-linux-extras install -y rust1
yum install -y openssl-devel libffi-devel python3-devel
pip3 install -U pip
pip install docker-compose
docker-compose version
```

Ref is [here](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html)