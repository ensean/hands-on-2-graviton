## Install Redis on Amazon Linux 2/2023


`You should consider AWS Elasticache Redis as a first choice for Redis`

1. Enviroment preparation

```
sudo yum update
sudo yum groupinstall "Development Tools" -y
```

2. Install from source

```
wget https://download.redis.io/redis-stable.tar.gz
tar -xzvf redis-stable.tar.gz
cd redis-stable
make
```

## Ref

* https://redis.io/docs/getting-started/installation/install-redis-from-source/