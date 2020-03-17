# Ansible Lab 9 - Add the Database Server

We've learned a lot so far. Let's see if we can add the mysql role and get a database up and running.

## Setup mysql-server on the Database Server
1. Add python-pip to common installation items.
2. Create mysql role using ansible-galaxy.
3. Create tasks and handlers for new mysql role.
5. Run playbook
6. Test a mysql connection to database


``` shell
ansible-galaxy init roles/mysql
ansible-playbook -i inventories/prod -K playbook1.yml --tags database
ssh db01
sudo /usr/bin/mysql -u root -p
```
