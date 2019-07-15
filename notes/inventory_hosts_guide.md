#### Guide to setup inventory hosts and groups

- Inventory with single group(demo) with one host

<b>inventory.txt</b>
```
[demo]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com
```

- Inventory with single group(demo) with one host containing alias and inventory variables

<b>inventory.txt</b>
```
[demo]
instance1 ansible_host=ec2-x-x-x-x.us-east-x.compute.amazonaws.com ansible_port=22 ansible_user=ec2-user ansible_ssh_private_key_file= # path to the private key
```

- Inventory with two groups(demo & demo1) with one host under each group

<b>inventory.txt</b>
```
[demo]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[demo2]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com
```

- Inventory with one groups(demo) with one host and its group inventory variables

<b>inventory.txt</b>
```
[demo]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[demo:vars]
ansible_user=ec2-user
ansible_pasword=password
ansible_ssh_private_key_file= # path to the private key
ansible_port=22
```

- Inventory with two groups and one children group with one host under each group

<b>inventory.txt</b>
```
[us-east-1a]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[us-east-1b]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[us-east-2a]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[us-east-2a]
ec2-x-x-x-x.us-east-x.compute.amazonaws.com

[us-east-1:children]
us-east-1a
us-east-1b

[us-east-2:children]
us-east-2a
us-east-2b
```

##### Test the remote hosts connectivity using ping module

```sh
export ANSIBLE_HOST_KEY_CHECKING=false
ansible -i inventory.txt -m ping
```
