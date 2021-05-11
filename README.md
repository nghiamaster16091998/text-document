$ sudo useradd -s /bin/bash -d /opt/stack -m stack

$ sudo su - stack

$ echo "stack ALL=(ALL) NOPASSWD: ALL" | sudo tee /etc/sudoers.d/stack
$ sudo su - stack

$ git clone https://opendev.org/openstack/devstack
$ cd devstack

[[local|localrc]]
ADMIN_PASSWORD=secret
DATABASE_PASSWORD=$ADMIN_PASSWORD
RABBIT_PASSWORD=$ADMIN_PASSWORD
SERVICE_PASSWORD=$ADMIN_PASSWORD

$ ./stack.sh
