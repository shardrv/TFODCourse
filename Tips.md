# Mostly used commands

## Creating virtualenv
```
virtualenv --python=/usr/bin/python3.8 venvnew
```

## Uninstalling CUDA


For CUDA 10.1 or newer, try:
```
sudo /usr/local/cuda/bin/cuda-uninstaller
```

For CUDA 10.0, try:
```
sudo  /usr/local/cuda/bin/uninstall_cuda_10.0.pl
```

## Installing

https://medium.com/@exesse/cuda-10-1-installation-on-ubuntu-18-04-lts-d04f89287130



## To completely uninstall Docker:

### Step 1

dpkg -l | grep -i docker

To identify what installed package you have:

### Step 2

sudo apt-get purge -y docker-engine docker docker.io docker-ce docker-ce-cli
sudo apt-get autoremove -y --purge docker-engine docker docker.io docker-ce  

The above commands will not remove images, containers, volumes, or user created configuration files on your host. If you wish to delete all images, containers, and volumes run the following commands:

sudo rm -rf /var/lib/docker /etc/docker
sudo rm /etc/apparmor.d/docker
sudo groupdel docker
sudo rm -rf /var/run/docker.sock

## Additionally

sudo apt-get purge -y docker-scan-plugin

sudo apt-get purge -y docker-ce-rootless-extras


You have removed Docker from the system completely.


