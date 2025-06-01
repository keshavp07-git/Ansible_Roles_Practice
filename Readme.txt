1. In Ansible Project Run Command -> ansible-galaxy init post-install
2. It will create directory with structure
3. Now Open main Playbook.yaml and Start dividing
4. Copy all variables from vars and variable yml to post-install/vars/main.yml
5. same for all handler copy handler part to post-install/handlers/main.yml
6. Same for task copy all to post-install/tasks/main.yml
# Do changes in path no need to define full path from this - templates/conf to conf.j2 ---j2 is standard for doing but not mandatory
7. Changes file name conf to conf.j2
8. src: files/my.txt to src: my.txt
9. To execute multiple roles syntax will be :-
roles:
  - post-install
  javaruntime_using_galaxy_link_third_party_from_galaxy_website
    role:
      - post-install
      - handlers

Important Points
1. In Playbook variable have highest priority
2. In var folder with main.yml have 2nd highest priority
3. In defaults folder with main.yml have lowest priority

Remove spaces in vim use :%s/  no. of space// press enter to remove empty spaces

Run --> ansible-playbook -i inventory.yaml prov.yaml
