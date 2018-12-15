# Kochiku::VPS

## Prerequisite

+ ansible 2.0 or higher

There are several ways to install Ansible. If you are running on a Mac OS X, it is easiest to install install through [Homebrew/homebrew](https://github.com/Homebrew/homebrew).

Check [ansible/ansible](https://github.com/ansible/ansible) for detailed installation instruction.

## Prepare vagrant box

The easiest way to use a box is to add a box from the publicly available catalog from [Vagrant Cloud](https://app.vagrantup.com/boxes/search). This Vagrantfile will automatically downloads CentOS Linux 7/x86_64 Vagrant images. To get started run:

```console
$ vagrant up
```

## Check the installation

```console
$ ansible -i development 192.168.33.10 -m ping
192.168.33.10 | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```

## Provision server with ansible

```console
$ ansible-playbook -i development playbook.yml --extra-vars "app_name=<your application name>"
```
