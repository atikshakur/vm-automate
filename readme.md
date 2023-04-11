# Automating multiple servers with ansible. Can be used to automate virtually any workflow

## Install ansible

```
sudo apt install ansible
```

## Install sshpass

```
sudo apt install sshpass
```

## Ping the hosts

```
ansible -i ./inventory/hosts ubuntu -m ping --user admin --ask-pass
```

## To update all hosts

```
ansible-playbook ./playbooks/apt.yml --user admin --ask-pass -ask-become-pass -i  ./inventory/hosts
```

## To install mysql

```
ansible-playbook ./playbooks/mysql.yml --user admin --ask-pass -ask-become-pass -i  ./inventory/hosts
```
