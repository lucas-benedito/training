# Ansible 101
[Return to Main Page](https://github.com/lucas-benedito/training)

How to install Ansible
```
$ dnf install ansible-core
```
Verify the installation
```
$ ansible --version
```

Create your inventory
```
$ vi inventory
[labnodes]
node1 ansible_user=root
```

Check your inventory with the ansible-inventory command
```
$ ansible-inventory -i inventory --list
```

Execute an ansible ping
```
$ ansible all -i inventory -m ping --ask-pass
```

Executing commands to a specific group/node
```
$ ansible labnodes -i inventory -m ping --ask-pass
$ ansible node1 -i inventory -m ping --ask-pass
```