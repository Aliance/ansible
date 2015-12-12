# Ansible configuration for local needs

This configuration helps to install all required programs as fast as it could be.
For example, after the OS reinstall or buying a new PC.

## Prerequisite

First of all, you need to install ansible itself:

```bash
$ sudo apt-get install -y -q ansible
```

After the ansible was installed, you can check it version (`ansible --version`) and execute the commands below into this repository directory:

## Test availability

You can execute ansible module `ping` on localhost machine:

```bash
ansible -m ping -c local -i hosts local
```

In case of success it will outputs:

```
localhost | success >> {
    "changed": false, 
    "ping": "pong"
}
```

## Install all required programs

To install all required programs, you can execute `install.yml` playbook:

```bash
$ ansible-playbook -c local -i hosts install.yml
```
