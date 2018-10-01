AWS-EC2-SITE
=========

A simple role to create webserver CI in AWS.

Requirements
------------

boto package is required, for AWS modules to work. Also, proper AWS settings need to be applied in default/main.yml.

Role Variables
--------------
vault_aws_access_key_id: AWS key ID
vault_aws_access_secret: AWS Access secret
aws_region: The AWS region that will be used
aws_ec2_group_name: EC2 group name
aws_ec2_group_description: EC2 group description
aws_vpc_id: AWS VPC ID
aws_instance_type: Instance type (t2.micro)
aws_ssh_keypair: Name of SSH Keypair in AWS
aws_ami: Which AMI image?
aws_vpc_subnet_id: AWS default subnet for public IP 
aws_admin_ssh_key: Path to pre-existing public SSH key - to be uploaded in AWS for management purposes.

Dependencies
------------

N/A

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
