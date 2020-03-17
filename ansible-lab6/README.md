# Ansible Lab 6 - Using Tags

Tags allow you to categorize items in your playbooks and tasks.  

1. Use --list-tags to see the current tags enabled.
2. Start adding tags to your playbooks and tasks. Make use of the 'always' keyword for common task of copying hostfile
3. Use --list-tags again to see the now enabled tags, and see tag inheritance.
4. Run your playbooks using tags to only run certain items

## Check Current Tags
``` shell
ansible-playbook -i hosts -K playbook1.yml --list-tags
``` 

## Run Playbook for Specific Tags
``` shell
ansible-playbook -i hosts -K playbook1.yml --tags configuration
ansible-playbook -i hosts -K playbook1.yml --tags proxy
```

### Notes:

Tags use "OR" logic, not "AND". If any of your tags match the item will run. You should use unique tags if the item should only be run under specific conditions.

Special tags: always, never.  Meaning "always" run or "never" run unless explicitly told to do so.
Special tag keywords: tagged, untagged and all.  By default we run playbooks at -tags all
