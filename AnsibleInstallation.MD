Steps to install and setup ansible

1) Install python on master
    sudo -i

    apt update -y

    apt-get install python3 -y

    python3 --version

2) Install Ansible on master
    apt-get update

    apt-get install software-properties-common

    apt-add-repository ppa:ansible/ansible

    apt-get update

    apt-get install ansible

    ansible --version

3) Create a public key for master
    ssh-keygen -t rsa     (Creates public and private key at /root/.ssh)

    /root/.ssh/id_rsa      => private key
    /root/.ssh/id_rsa.pub  => public key
    
4) Copy content of public key from /root/.ssh/id_rsa.pub of ansible master using cat command
    cat /root/.ssh/id_rsa.pub
    copy file content from here

5) Paste content in /root/.ssh/authorized_keys of agent/node using vim editor
    vim /root/.ssh/authorized_keys
    paste the content here
    then press Esc
    then press :wq! and enter

6) Add ip/DNS of nodes/agents into the inventory file of ansible master in /etc/ansible/hosts using vim editor
    vim /etc/ansible/hosts
    paste public ip / private ip of nodes here

7) To check connections with nodes use command
     ansible -m ping all
