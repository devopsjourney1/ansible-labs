# Ansible Lab 1 - Inventory file basics

1. Copy /vagrant/hosts_file to /etc/hosts 
2. Install ansible
3. Create an inventory file named hosts
4. Test out a command
5. Generate SSH Keys and copy to hosts
6. Test running commands to all hosts
7. Install python-simplejson module. This allows clients to be fully managed.

### Setup Vagrant and connect to ansible-control server
``` shell
 vagrant up
 vagrant ssh ansible-control
```


### Copy hosts file on ansible-control
``` shell
cp /vagrant/hosts_file /etc/hosts 
```

### Install Ansible
``` shell
 sudo apt-get install ansible
```

### Install Ansible
``` shell
ssh-keygen
ssh-copy-id localhost
ssh-copy-id web01 && ssh-copy-id web02 && ssh-copy-id loadbalancer && ssh-copy-id db01
```

### Install python-simplejson
``` shell
ansible all -i hosts -m command -a 'sudo apt-get -y install python-simplejson'
```
