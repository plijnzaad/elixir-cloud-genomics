elixir-cloud-genomics
=====================

Simple Ansible setup to deploy a training environment on an Ubuntu 14.04 virtual machine

To use this demo you will need:
 - Ansible 1.8:
   http://docs.ansible.com/intro_installation.html
 - Access to the virtual machine to configure

If you also want to deploy the machines, you need:
 - OpenStack command line tools:
   http://docs.openstack.org/user-guide/content/install_clients.html
 - Access to an OpenStack cloud
 - Your openstack RC file
   

Configuration:

You will need the IP or hostname of the machine(s) to configure. You will need the *hash* of the password to add. Check the demo.hosts file. 

This playbook automatically adds a user "joe" with the password configured password. To generate the password hash, run
mkpasswd -m SHA-512
Enter the desired password and copy the resulting string into demo.hosts. The mkpasswd utility can be found in the whois package.

To deploy the machines, verify the variables under vars in create-instance.yml, then run:
    ansible-playbook -i demo.hosts create-instance.yml

To configure the machines, run:
    ansible-playbook -i demo.hosts setup-instance.yml


