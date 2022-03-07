# ansible-ec2
This YAML file creates an ec2 instance using ansible.

Pre Requisites:
---------------
- Must have keypair created and uploaded to AWS.
- Must have ansible installed and proper IAM role given to the instance.


The ansible playbook is composed of 2 plays. 

Play 1:
---------------
A play to create a security group and an ec2 instance. 


Play 2:
---------------
A play to install apache as well as other packages and to configure a web page showing the local machine's ip.


Run:
---------------
ansible-playbook createEc2.yml
