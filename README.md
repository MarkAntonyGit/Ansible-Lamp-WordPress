# Ansible-Lamp-WordPress
Ansible Playbook to Setup Amazon Linux Server With a WordPress Website

## Description:
A simple ansible playbook to setup a wordpress website on amazon linux based servers with custom virtual host on apache webserver.  [Ansible](https://www.ansible.com) is an open-source software provisioning tool by [Red Hat](https://www.redhat.com/en). We can use Ansible for cloud provisioning, configuration management, application deployment etc. 

In this repo I have created a simple playbook to create a WordPress website with apache, MySQL database and PHP7.4 on Amazon Linux based servers. As of now this is just a experimental work on ansible palybook. But this can be edited to use for other linux OS families also. 

## Features:
- One step creation of website is desired number of servers. 
- Variables file to manage MySQL root password, WordPress database details etc.
- Can also specify major php ini settings like upload_max_filesize , memory_limit etc using variables file
- All the components are installed through the playbook like (Apache, MySQL, PHP, Wordpress)

## How to Use:
##### 1. Install Git and Ansible on Master Server.
```
yum install git -y
amazon-linux-extras ansible2 -y
```
##### 2. Clone this Repo and Create hosts file for ansible playbook and create key file
```sh
git clone https://github.com/MarkAntonyGit/Ansible-Lamp-WordPress.git
cd Ansible-Lamp-WordPress
Vim hosts (Add ansible client server details)
Vim keyfile.pem (Add private key file for ansible client servers)
chmod 600 keyfile.pem
```
-- Sample Hosts File 

![](https://i.ibb.co/XXQ3fW2/githosts.jpg)
 
##### 3. Edit Variables, Check Connection and Run Play
```
ansible -i hosts all -m ping (To check your master and client connection)
vim lamp_wp_variables.yml (To edit variables)
ansible-playbook -i hosts playbook_lamp_wordpress.yml --syntax-check 
ansible-playbook -i hosts playbook_lamp_wordpress.yml
```
--Sample Variables File

![](https://i.ibb.co/VN65rpC/git4.jpg)

## Sample Output Screenshots: 

--Play Outputs

![](https://i.ibb.co/t4bn4WJ/git2.jpg)
![](https://i.ibb.co/xFrGzyj/3.jpg)

--Website Outputs 

![](https://i.ibb.co/7KKqrVy/git3.jpg)
![](https://i.ibb.co/tzc80BT/2.jpg)

### If you are using a demo website name. Please use the following online tool for checking the website via hosts method or you can use the local hosts file of your PC. 
### https://hosts.cx/

### Connect with me

--------<img src="https://img.shields.io/badge/-Mark%20Antony-brightgreen"/> ----------------------------------------------------------------------------------------------------------------------------------- <a href="https://www.linkedin.com/in/profile-markantony/"><img src="https://img.shields.io/badge/-Linkedin%20Profile-blue"/></a> ------------------------------------------------------------------------------------------------------------------------------------ <a href="mailto:markantony.alenchery@gmail.com"><img src="https://img.shields.io/badge/-markantony.alenchery@gmail.com-D14836?style=flat&logo=Gmail&logoColor=white"/></a>-------------------------------------------------------

