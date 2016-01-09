## Prerequisite
+ ansible 1.9 or higher

There are several ways to install Ansible. If you are running on a Mac OS X, it is easiest to install install through [Homebrew/homebrew](https://github.com/Homebrew/homebrew).

Check [ansible/ansible](https://github.com/ansible/ansible) for detailed installation instruction.

## Prepare vagrant box
The easiest way to use a box is to add a box from the publicly available catalog from [Vagrantbox.es](http://www.vagrantbox.es/). This Vagrantfile will automatically downloads CentOS 6.4 x86_64 Minimal (VirtualBox Guest Additions 4.3.2, Chef 11.8.0, Puppet 3.3.1) provided by National Renewable Energy Laboratory (NREL).
To get started run:
```
$ vagrant up
```

## Check the installation
```
$ ansible -i development 192.168.33.20 -m ping
192.168.33.20 | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```
