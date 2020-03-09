# Ansible Lab 1 - Inventory file basics

1. Create an inventory file named.
2. Test out a command
3. Generate SSH Keys and copy to hosts
4. Test running commands to all hosts
5. Install python-simplejson module. This allows clients to be fully managed.

``` shell
 ansible control -i hosts -m command -a hostname
 ssh-keygen
 ssh-copy-id localhost
 ansible control -i hosts -m command -a hostname
 ssh-copy-id web01 && ssh-copy-id web02 && ssh-copy-id db01 && ssh-copy-id loadbalancer 
 ansible all -i hosts -m command -a date
 ansible all -i hosts -m command -a 'sudo apt-get -y install python-simplejson'
 sudo vi /etc/ansible/ansible.cfg
 /deprecation <to search for it, then remove the warning>
 ansible all -i hosts -m command -a date
 ansible all -i hosts -m command -a 'sudo apt-get -y install python-simplejson'
 ```