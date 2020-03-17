# Ansible Lab 7 - Ansible Variables

Two types of variables. User set and "ansible facts".

## Gather ansible facts, these are dynamic variables automatically gathered by ansible
1. Use setup module to gather facts about a system.
2. View the output and discovery any useful information
3. Use {{ ansible_facts['nodename'] }} for the nodename variable for the local host. Add this to the index.html file.
4. Use a loop to dynamically access the nodename of the two webservers. add this to the mysite configuration of nginx proxy server.


``` shell
ansible -i hosts proxy -m setup >> ansible_facts.json
{{ ansible_facts['nodename'] }}

	{% for host in groups['webservers'] %}
        server {{ hostvars[host]['ansible_facts']['nodename'] }}:8000;
    {% endfor %}
```

## Move user defined variables to a different location
1. Move your current variables into the group_vars/all variables
2. Add these variables to your nginx mysite configuration
3. Create host_vars folder and make a unique variable for web01
