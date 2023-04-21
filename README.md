# Ansible 101
[Return to Main Page](https://github.com/lucas-benedito/training)
Repository containing Training data

How to install Ansible
```
$ dnf install ansible-core
```

Create your inventory
```
$ vi inventory
node1 ansible_user=devops
```

Execute an ansible ping
```
$ ansible all -i inventory -m ping
```