# ansible-ec2
This YAML file creates an ec2 instance using ansible.

Pre Requisites:
---------------
- Must have keypair created and uploaded to AWS.
- Must have ansible installed (2.9.10) and proper IAM role given to the instance.
- Must have Python (2.7.5) , boto (2.4.9) , and botocore (1.6.8) installed


The ansible playbook is composed of 2 plays. 

Play 1:
---------------
A play to create a security group and an ec2 instance.
- Security Group:
  Creates a security group within a vpc with specific IP's allowed inbound over ssh and http connection.
- Ec2 Instance:
  Creates an ec2 instance with a given key pair and attaches the security group onto it.


Play 2:
---------------
A play to install apache as well as other packages and to configure a web page showing the local machine's ip.


Run:
---------------
ansible-playbook createEc2.yml
