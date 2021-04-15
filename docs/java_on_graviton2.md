## Java on graviton2

* OS: Amazon Linux 2

* Steps to setup Java environment

```
sudo amazon-linux-extras enable corretto8
sudo yum clean metadata
sudo yum install -y java-1.8.0-amazon-corretto-devel
sudo yum install fontconfig -y     # To avoid awt font not support error
```