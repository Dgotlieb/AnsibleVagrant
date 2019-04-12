# Ansible Vagrant
A simple Vagrantfile for Ansible

### Prerequesits:
* Git
* Oracle Virtual box
* Vagrant

#


### Vagrantfile Job:
1. Creates an Ubuntu 18.04 VM with 2 CPU's and 2048 MB Ram memory
2. Installs Ansible

# 

### Initial setup:
1. Clone this repository:
    $ git clone https://github.com/Dgotlieb/AnsibleVagrant.git 
2. cd to internal folder:    
    $ cd AnsibleVagrant-master/Ansible/
3. In **keys** folder - replace the priavte key with your server key (e.g. EC2)
4. In **hosts** folder:
    * Change the IP address to the IP address of the machine/s you want to control.
    * Change the user name to the user name of the machine/s you want to control
5. Start nachine:
    $ vagrant up
6. SSH into machine
    $ vagrant ssh
7. Run:
    $ sudo ansible all -m ping
#

### Importana note:
In case, the machine uses python3, you will need to add the python interpreter version to your host/s:
 192.168.99.100 ansible_ssh_private_key_file=private.pem ansible_user=ec2-user **ansible_python_interpreter=python3**

 

