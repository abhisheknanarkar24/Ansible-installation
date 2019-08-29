# Ansible-installation
This repository contains Ansible installation steps from scratch.

1. Ansible Dependencies Installation

Ansible setup requires certain packages like python, sshpass, and so on, to be installed on the Ansible Orchestration Server. See the following list:

python-crypto

python-httplib

python-jinja2

python-keyczar

sshpass

python-pip

python2-winrm


These dependencies can be found in /ansiblerepo folder

Note: Installation of all these packages can be efficiently done by either having all these RPMs in a shared repository or in the case where this is  not available, create a local yum repository. This is because the RPMs are dependent on each other and installing them individually can be a lengthy process. 

2. Installation

Once the repository is in place, execute the following steps:
Copy the rpm to the server and install it using the below command:

$ sudo yum -y install python-cryptography

$ sudo yum -y install python-httplib2

$ sudo yum -y install python-jinja2

$ sudo yum -y install sshpass

$ sudo yum -y install python-keyczar

$ sudo yum -y install python-pip

$ sudo yum -y install python2-winrm

$ sudo yum -y install ansible


Note:
Ansible installation creates a directory /etc/ansible that is owned by the root user by default. Ensure that after the installation is complete, the owner should be changed to your current user if required (depends on your requirement).

3. Verify the installation using the following command:


$ ansible --version



You will be presented with the following output:


ansible 2.5.2

  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/home/<username>/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  
  ansible python module location = /usr/lib/python2.7/site-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.5 (default, Sep 12 2018, 05:31:16) [GCC 4.8.5 20150623 (Red Hat 4.8.5-36)]


