# mathoid

Vagrant machine to configure an Ubuntu Trusty 14.04 64-bit box with Mathoid based on Node.js & Phantomjs Chef Solo scripts.

## Install Vagrant & VirtualBox

### Install Vagrant:
[http://vagrantup.com](http://vagrantup.com)

### Install VirtualBox:
[https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

## Provision a VM

```
git clone git@github.com:cbumgard/mathoid-vagrant.git
cd mathoid-vagrant
git submodule init
git submodule update
vagrant up
vagrant ssh
```
