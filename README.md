# AnsibleDockerGoTest

Dockerized Go App

## Prerequisites ##

* Vagrant
* VirtualBox
* Ansible


Install Ansible

```
$ sudo easy_install pip
```

```
$ sudo pip install ansible
```

Install Ansible Docker Plugin
```
ansible-galaxy install angstwad.docker_ubuntu
```


Launch Vagrant

```
$ vagrant up
```

Manual Ansible Provision
```
$ ansible-playbook -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory --private-key=.vagrant/machines/default/virtualbox/private_key -u vagrant playbook.yml
```

## Go App ##
```
$ vagrant ssh
```
```
$ cd /vagrant/app
```

Available at `http://localhost:8080/`


