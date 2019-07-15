## Ansible installation in Ubuntu


```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:ansible/ansible
$ sudo apt-get update
$ sudo apt-get install ansible
```

#### To Test the ansible installation

```
$ ansible --version
ansible 2.8.2
  config file = None
  configured module search path = ['/Users/barath/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/local/Cellar/ansible/2.8.2/libexec/lib/python3.7/site-packages/ansible
  executable location = /usr/local/bin/ansible
  python version = 3.7.4 (default, Jul  9 2019, 18:13:23) [Clang 10.0.1 (clang-1001.0.46.4)]
```
