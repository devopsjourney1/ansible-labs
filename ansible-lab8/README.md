# Ansible Lab 8 - Create a Developement/Production inventory file

You can have multiple sets of inventories. Let's create a production and developement inventory file and set a variable for them.

## Gather ansible facts, these are dynamic variables automatically gathered by ansible
1. Create inventories directory.
2. Create an inventory file for dev and production.
3. Set a enviornement variable and run the playbook.


``` shell
ansible-playbook -i inventories/dev -K playbook1.yml
ansible-playbook -i inventories/prod -K playbook1.yml
```
