## Java on graviton2

* OS: Amazon Linux 2

* Steps to setup Java environment

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
. ~/.nvm/nvm.sh
nvm list-remote --lts   # list all the LTS versions
nvm install v10.24.1    # Install the target node version
node -v                 # check if node works
```