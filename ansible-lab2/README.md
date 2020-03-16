# Ansible Lab 2 - Ad HOC tasks and Modules


1. Run Ad hoc tasks using APT module
2. --become gives you root access. Same as running the command with "sudo"
3. Use service module to manage services
4. Run command to reboot web servers

``` shell
ansible all -i hosts --become -m apt -a "update_cache=yes"
ansible web -i hosts --become -m apt -a "name=apache2 state=present"
ansible database -i hosts --become -m apt -a "name=mysql-server state=present"
ansible proxy -i hosts --become -m apt -a "name=nginx state=present"
ansible database -i hosts -m service -a "name=mysql state=started"
ansible database --become -i hosts -m service -a "name=mysql state=restarted"
ansible web -i hosts --become -a "reboot --reboot"
 ```

 ansible all -i hosts --become -m apt -a "update_cache=yes"