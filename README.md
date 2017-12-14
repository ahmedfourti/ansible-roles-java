Role Name: Java
===============

This is a basic role to install Java in your systems.

Requirements
------------

No requirements   

Role Variables
--------------

**java_packages_redhat**: Java version for Redhat systems.     
**java_packages_debian**: Java version for Debian systems. 

Installation
------------

You can get this role by using ```git clone``` command.  
You can also add this repo to your ```requirements.yml``` and use ```ansible-galaxy install -r requirements.yml -p {{path_to_roles}}```  
Or you can download and unzip it in your roles directory 

Example Playbook
----------------



    ---
       - name: Deploying Demo
         hosts:
           - web-debian
           - web-centos
         become: yes
         roles:
           - java
         vars:
           #Role Java
           java_packages_redhat:
             - java-1.8.0-openjdk
           java_packages_debian:
             - openjdk-8-jdk

License
-------

BSD