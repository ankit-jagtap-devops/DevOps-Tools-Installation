Steps to install and setup ansible
1) Install python on master

2) Install Ansible on master

3) Create a public key for master
    ssh-keygen -t rsa     (Creates public and private key at /root/.ssh)
    
4) Copy content of public key from /root/.ssh/id_rsa.pub of ansible master 

5) Paste content in /root/.ssh/authorized_keys of agent/node using vim editor

6) Add ip/DNS of nodes/agents into the inventory file of ansible master in /etc/ansible/hosts using vim editor

7) To check connections with nodes use command
     ansible -m ping all