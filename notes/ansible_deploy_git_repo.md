### Deploying From Source Control
Deploy your webapp straight from git

```
$ ansible web -m git -a "repo=https://github.com/BarathArivazhagan/spring-boot-demo.git dest=/home/centos/spring-boot-demo" -u centos
```

This will copy the git repo from the source and place it into the destination path
