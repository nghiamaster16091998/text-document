$ sudo apt-get update

$ sudo useradd -s /bin/bash -d /opt/stack -m stack

$ sudo su - stack

$ echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack

$ sudo su - stack

$ sudo apt install git

$ git clone https://opendev.org/openstack/devstack

$ cd devstack

$ cd samples

$ cp local.conf ../

$ cd ..

$ sudo nano local.conf

[[local|localrc]]

ADMIN_PASSWORD=secret

DATABASE_PASSWORD=$ADMIN_PASSWORD

RABBIT_PASSWORD=$ADMIN_PASSWORD

SERVICE_PASSWORD=$ADMIN_PASSWORD

HOST_IP = 192.168.2.132

$ ./stack.sh

https://www.youtube.com/watch?v=sJ92sWgEAd8&t=183s&ab_channel=MahmoudHussein
