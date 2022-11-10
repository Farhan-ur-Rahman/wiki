---
{}
---
   
**#ANSIBLE**   
   
     
    
     
   
**Playbook**   
   
it uses YAML (YET ANOTHER MARKUP LANGUAGE) scripting that uses in playbook to write codes.   
   
     
   
Playbook is like a file where you can write codes  that consists of variables, tasks, handlers   
   
     
   
Each playbook is composed of one or more ‘modules’ in a list. Module is a collection of configuration files   
   
     
   
Playbook are divides into many section s like-   
   
     
   
**target section - Defines that host against which playbook task has to be executed**   
   
     
   
**variable section - Defines variable**   
   
     
   
**Task it performs the process of all modules that we need to run in order**   
   
     
   
Overviewed the codes inn playbook practically in ansible server    
   
     
   
**Ansible Roles,Conditions**   
   
     
   
     
   
 **- - - # Condition Playbook**   
   
     
   
   
-   **host: demo**   
   
       **user: ansible        TARGET  SECTION**   
   
       **become: yes**   
   
       **connect : ssh**   
   
     
   
**name: install apache on debian**   
   
**command: apt-get -y install apache2**   
   
**when: ansible_os_family == “Debian”**   
   
**name: install apache for  red-hat**   
   
     
   
**Ansible uses the push mechanism from the nodes**