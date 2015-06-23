This file describes the steps that have to be taken before running the workshop with `elixir-cloud-genomics` lesson.
You (the taecher) need to have access to cloud interface and create virtual machines that can be used during the workshop. 

Folowing software is expected to be available on the vm that students used:
* Ubuntu 14.04
* Java (eg. openjdk-7-jdk)
* wget
* htop

#Setting up the virtual machines
Ideally there is single vm per student.

Creation of the virtual machines will depend on the infrastructure. Here are some examples:
* [OpenNebula](http://opennebula.org/documentation/) (used by SurFSARA, Netherlands)
* [OpenStack](http://docs.openstack.org/) (used by CSC, Finland)
* [iPlant's Atmosphere](http://www.iplantcollaborative.org/ci/atmosphere)
* [XSEDE](https://www.xsede.org/high-performance-computing)
* [Amazon Web Services](https://aws.amazon.com/documentation/)
* [Google Compute Engine](https://cloud.google.com/docs/)
* [Digital Ocean](https://www.digitalocean.com/help/)

## using Ansible
There are many ways to automate setting up multiple machines for the workshop. Please find included exmple with [Ansible](http://www.ansible.com/home).
* `create-instance.yml` contains Ansible description for starting up multiple vm machines on OpenStack based cloud.
* `setup-instance.yml` contains Ansible description for installing necessary software on vms
