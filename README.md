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

SERVICE_HOST=$HOST_IP

MYSQL_HOST=$HOST_IP

RABBIT_HOST=$HOST_IP

GLANCE_HOSTPORT=$HOST_IP:8080

$ ./stack.sh

https://www.youtube.com/watch?v=sJ92sWgEAd8&t=183s&ab_channel=MahmoudHussein

https://docs.openstack.org/devstack/latest/

https://www.youtube.com/watch?v=p_6jYq9BWYE&t=224s&ab_channel=KushalBhavsar

https://discord.com/channels/740829801446637601/811692671751159869/852854995191726080
