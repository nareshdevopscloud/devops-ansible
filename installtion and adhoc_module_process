----------------------ansible----------------

sudo yum update -y

sudo yum install ansible -y

ssh-keygen --copy public ip and paste it into target server path .ssh/authorizedkeys 

-----------------------sample ad-hoc coomand -------------------
Ad-hoc commands are commands which can be run individually to perform quick functions

inventory: An inventory is a list of managed nodes, or hosts, that Ansible deploys and configures. 
This guide introduces you to inventories and covers the following topics: Creating inventories to track a list of servers and devices that you want to automate

Inventory default path sudo /etc/ansible/hosts

if target node will add in default path no need to pass '-i inventory' in command it will fetch autometically from default path

vi inventory 

add target private ip

ansible -i inventory all -m "shell" -a "touch file1"




ansible-modeules ad-hoc commands 

 
----ping module-------
ansible -i inventory all -m ping 

-----stat module ----
ansible -i inventory all -m stat -a "path=/var/www/html"

------yum or apt module -----

ansible -i inventory all -m yum -a "name=httpd state=present"    

----------user----------

ansible -i inventory all -m user -a "name=naresh" -b

-----------setup--------
ansible -i inventory all -m setup

---------------file------------
ansible -i inventory all -m file -a "name=demo state=touch"

---------------copy-------------
ansible -i inventory all -m copy -a "src=file1  dest=~"
----------------------



(basic state's
name = (httpd install)
               state=latest
               state=present
               state=absent )

ansible all -m yum -a "name=httpd state=latest" -b
ansible all -m yum -a "name=httpd state=present" -b
ansible all -m yum -a "name=httpd state=absent" -b

(name = systemctl or service              
               state=stopped
               state= started
               state=restrted)
ansible all -m service -a "name=httpd state=started" -b      #to start service

ansible all -m service -a "name=httpd state=stopped" -b       #to stop service 

ansible all -m service -a "name=httpd state=restrted" -b       #to stop service 

