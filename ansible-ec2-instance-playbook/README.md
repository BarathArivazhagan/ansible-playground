## Ansible playbook to create AWS EC2 instance 

Note : AWS credentials has to be setup and boto package has to be installed before executing the ansible playbook

```
$ ansible-playbook ansible-ec2-instance.yaml
```

##### To install boto package:

```
$ sudo apt-get install python-boto
```

Tip: Execute the playbook within EC2 instance with EC2FullAccess role attached without exposing the aws credentials to avoid security threats
