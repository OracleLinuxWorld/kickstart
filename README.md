# kickstart
Oracle Linux kickstart installation scripting


Steps to install a DHCP / PXE netboot / kickstart installation server perform the following steps
on you local machine:

* Install Ansible on your local machine
* Clone this project locally
* After cloning, check and/or change the variables in the file: inventory/group_vars/pxeserver
* Change the IP address mentioned in the inventory/hosts file 


You can then run the Ansible runbook as follows:

   ansible-playbook -i inventory/hosts setup-pxeboot-server.yml

After this you should have a fully working DHCP/PXE/Kickstart installation environment
for installing Oracle Linux 6.9 and 7.4 servers.


Changes to be done on the intended target:

* Do *not* forget to mount the installation DVD ISO (file) for Oracle linux 6.9 / 7.4 under the /cdrom mountpoint 
  before attempting to provision Oracle Linux servers.
