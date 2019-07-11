### Simple Ansible Commands 

#### Inventory Hosts

create a inventory hosts file and add hosts/groups as shown below with remote host details
```
vi inventory.txt

# some hosts ungrouped
10.0.0.1
10.0.0.2

# some hosts grouped with group name demo
[demo]
10.0.0.3
10.0.0.4

```

##### ping module

```
ansible all -i inventory.txt -m  ping -u user  # To ping the group of hosts present in /etc/ansible/hosts
```

##### file module

```
ansible all -i inventory.txt -m file -a "dest=/dest/path state=directory"
```

##### copy module

```
ansible all -i inventory.txt -m copy -a "src=/source/path dest=/destpath"
```

##### yum module

```
ansible all -i inventory.txt -m yum -a "name=docker state=present" -become=true
```
##### systemd module

```
## start
ansible all -i inventory.txt -m systemd -a "name=docker state=started" -become=true

## stop
ansible all -i inventory.txt -m systemd -a "name=docker state=stopped" -become=true
```
##### service module

```
## start
ansible all -i inventory.txt -m service -a "name=docker state=started" -become=true

## stop
ansible all -i inventory.txt -m service -a "name=docker state=stopped" -become=true
```

