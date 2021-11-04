# Mostly used commands

## Creating virtualenv
```
virtualenv --python=/usr/bin/python3.8 venvnew
```

ImportError: No module named pkg_resources: the solution is to reinstall python pip using the following Command are under.

```
Step: 1 Login in root user.

Step: 2 Uninstall python-pip package if existing.

sudo apt-get purge -y python-pip
Step: 3 Download files using wget command(File download in pwd )

wget https://bootstrap.pypa.io/get-pip.py
Step: 4 Run python file.

sudo -H python3 ./get-pip.py
Step: 5 Finaly exicute installation command.

sudo apt-get install python-pip
```

ImportError

## For using virtualenv kernel inside the jupyter notebook
```
python -m ipykernel install --user --name=venv
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


sudo systemctl daemon-reload
sudo systemctl restart docker

## NVIDIA CONTAINER
https://github.com/NVIDIA/nvidia-container-runtime

## Protobuf

https://github.com/protocolbuffers/protobuf/blob/master/src/README.md

http://google.github.io/proto-lens/installing-protoc.html

This one here

https://github.com/protocolbuffers/protobuf/blob/master/src/README.md




# Inside Docker for Object Detection tf3d

pip3 install gin-config

pip3 install tensorflow-datasets

pip3 install tensorflow_probability==0.11.0

pip3 install shapely

pip3 install object_detection

Error
    from object_detection.protos import string_int_label_map_pb2
ImportError: cannot import name 'string_int_label_map_pb2'


# Installing protobuf
https://github.com/protocolbuffers/protobuf/blob/master/src/README.md

# Running gsutil conflicts with another package

Do a *which gsutil*

cd into the directory 

Run the gsutil using ./gsutil ........

https://medium.com/codex/how-to-use-gsutil-and-python-to-deal-with-files-in-google-cloud-storage-fc4f430b3b28


# To enable GPU need to access -> software-properties-gtk
## Issue cannot open the gtk

Reinstall python3-six && python3-dateutil

```
sudo apt install python3-dateutil --reinstall
sudo apt install python3-six --reinstall

```
# ROS STUFF

Helped in quaternions  conversion

https://gist.github.com/LimHyungTae/2499a68ea8ee4d8a876a149858a5b08e

http://wiki.ros.org/tf2/Tutorials/Quaternions

https://stackoverflow.com/questions/55150211/how-to-calculate-relative-pose-between-two-objects-and-put-them-in-a-transformat

https://answers.ros.org/question/332407/transformstamped-to-transformation-matrix-python/

https://github.com/wsnewman/learning_ros/blob/master/Part_2/example_tf_listener/src/example_tf_listener_fncs.cpp

# When the compiler says no cuda found - please add in path do this
```
export CUDA_HOME=/usr/local/cuda
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64:/usr/local/cuda/extras/CUPTI/lib64
export PATH=$PATH:$CUDA_HOME/bin
```
