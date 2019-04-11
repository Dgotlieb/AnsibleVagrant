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

    $ git clone https://github.com/Dgotlieb/AnsibleVagrant.git 
    $ cd AnsibleVagrant-master/Ansible/
    $ vagrant up
    
    
### How to use:
 
##### Hosts / Inventory

1. Go to /etc/ansible/hosts.
2. Change the IP address to the IP address of the machine/s you want to control.
3. Change the user name to the user name of the machine/s you want to control
4. in case, the machine uses python3, you will need to add the python interpreter version to your host/s:
 
 192.168.99.100 ansible_ssh_private_key_file=private.pem ansible_user=ec2-user **ansible_python_interpreter=python3**

 #
 
##### Keys: 
1. Go to /etc/ansible/keys.
2. Replace the file private.pem with the private key of the machine/s you want to control.
3. Run: $ chmod 400 private.pem

#### Run: **ansible all -m ping**
 
 #
 

