# ansible
role-kafka-nginx-postgresql-node.js


Ansible Roles are a way to group related tasks, files, variables, and other assets in a standardized file structure. They are a key feature of Ansible that allows users to reuse and share their Ansible code efficiently

Here are some benefits of using Ansible Roles: 
Reuse: Roles can be reused across playbooks and in many projects without duplicating code. 
Share: Roles can be shared with other users in collections. 
Modularization: Roles facilitate modularization of configuration. 
Efficiency: Roles provide a well-defined framework for setting tasks, variables, and other files. 


Ansible Role 

Private IPv4 addresses 172.31.87.199

$ ansible all -m ping 
$ ansible all -m copy -a "src=/tmp/dump.sql dest=/tmp/dump.sql"


# Basic PostgreSQL command
https://www.w3schools.com/postgresql/postgresql_insert_into.php

$ psql --version
$ sudo apt install postgresql-client-common
$ sudo apt-get install -y postgresql-client
$ sudo -u postgres psql


# copy file form Local machine to remote machine(ubuntu)
$ scp -r \Users\SATYA\Downloads\ansible-role ubuntu@3.85.183.89:~/  


---
- hosts: nginx
 become: yes
 become_user: root
 become_method: sudo
 roles:
   - nginx

- hosts: postgresql
 become: yes
 become_user: root
 become_method: sudo
 roles:
   - postgresql

- hosts: kafka
  become: yes
  become_user: root
  become_method: sudo
  roles:
    - kafka

- hosts: nodejs
 become: yes
 become_user: root
 become_method: sudo
 roles:
   - nodejs