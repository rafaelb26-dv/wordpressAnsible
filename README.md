# Infrastructure as Code Project
Configure a virtual machine using Vagrant and Ansible to receive a WordPress instance

# Project structure
files/00-default.conf -> Apache config file to serve the application

files/my.cnf -> Configuration file used to make the connection between the Database VM and the Wordpress VM

group_vars/all.yml -> This file receives all environment variables and sensitive data values

hosts -> File that contains the necessary information to be able to access the VM's by SSH

provisioning.yml -> Environment configuration file that installs all the necessary dependencies for Wordpress to work

Vagrantfile -> File to provision two VM's, one for the database and one for wordpress


# To run this project you need to have vagrant and ansible installed.
Follow the links to install Vagrant and Ansible on Linux ubuntu:

https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-22-04     
https://itslinuxfoss.com/install-vagrant-ubuntu-22-04/

After installing Ansible and Vagrant, clone the project to your machine, open your favorite text editor and replace the values ​​of the variables that are in the files "all.yml, hosts and Vagrantfile"

# To build the project, run the following commands:

"vagrant up wordpress"

"vagrant up mysql"

"ansible-playbook provisioning.yml -i hosts"

Access application with wordpress private ip that was defined in Vagrantfile






