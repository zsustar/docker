# Install on Ubuntu

- Reference 
https://docs.docker.com/install/linux/docker-ce/ubuntu/

- OS requirements  
64-bit version of one of these Ubuntu versions:

  - Bionic 18.04 (LTS)
  - Xenial 16.04 (LTS)
  - Trusty 14.04 (LTS)
- Start the Installation

```
#uninstall old version
sudo apt-get remove docker docker-engine docker.io

sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

#Add Docker’s official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - 

#set up the stable repository
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

#Start to Install Docker CE
sudo apt-get update
sudo apt-get install docker-ce

# I
#List the versions available in your repo:
apt-cache madison docker-ce
```
- post installation
```
sudo groupadd docker
sudo usermod -aG docker $USER
docker run hello-world
```

- upgrade dokcer
```
sudo apt-get update
```
- hostname
hostnamectl set-hostname 
ssh-keygen -b 2048 -t rsa -f ~/.ssh/id_rsa -q -N ""

# Install on RedHat
```
#Uninstall old version
sudo yum remove docker \
                  docker-client \
                  docker-client-latest \
                  docker-common \
                  docker-latest \
                  docker-latest-logrotate \
                  docker-logrotate \
                  docker-selinux \
                  docker-engine-selinux \
                  docker-engine \
                  docker-ce
#install required package
sudo yum install -y yum-utils \
  device-mapper-persistent-data \
  lvm2

#setup stable repo
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

#Start CE Installation 
sudo yum install docker-ce

#Start Docker.
sudo systemctl start docker
```
# Install on Mac
https://docs.docker.com/docker-for-mac/install/#install-and-run-docker-for-mac

# Install on Windows
https://docs.docker.com/docker-for-windows/install/#about-windows-containers
