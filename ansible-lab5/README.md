# Ansible Lab 5 - Roles and Ansible Galaxy

ansible-galaxy allows you to download roles and also provides an excellent default framework for creating your own roles.

## Change Playbook so it uses the Role functionality to setup apache2
1. Use ansible-galaxy to create webserver role scaffolding
2. Move the tasks to the roles\webserver folder
3. Run playbook


### Create Apache2 Role, move tasks/handlers/templates to new roles/apache2 structure. Run playbook.
``` shell
ansible-galaxy init roles/apache2
ansible-playbook -i hosts -K playbook1.yml
```

### Create a 'common' Role and add it to 'web', 'loadbalancer' and 'database' servers

1. Use ansible-galaxy to create nginx role scaffolding
2. Setup tasks/main.yml and tasks/install_tools.yml
3. Run playbook and test

``` shell
ansible-galaxy init roles/nginx
ansible-playbook -i hosts -K playbook1.yml
```

### Create a nginx Role and setup the configuration

1. Use ansible-galaxy to create nginx role scaffolding
2. Setup tasks, handlers and templates

``` shell
ansible-galaxy init roles/nginx
ansible-playbook -i hosts -K playbook1.yml
```