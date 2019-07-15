# Steps to setup ansible inventory file

- create an inventory file 
```
[demo]
hostname1 or ip
hostname2 or ip

[demo:vars]
ansible_user=ec2-user
ansible_ssh_private_key_file=PATH TO PRIVATE KEY
```
