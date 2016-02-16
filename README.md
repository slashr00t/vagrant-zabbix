# Vagrant for Zabbix

This Vagrant configuration can be used for quick testing purposes of Zabbix infrastructure. All systems are based on **CentOS 7** (see Vagrantfile).
Current version supports also Zabbix in newest version **3.0**!

# Requirements
  * **Vagrant** (can be downloaded from [here](https://www.vagrantup.com/downloads.html))
  * **VirtualBox**
  * *(optionally)* **libvirt and KVM** (for advanced users)

# Usage

Just use vagrant to start zabbix server. From inside directory where you cloned this repository run the following command
```
vagrant up
```

After machine finished provisioning Zabbix you can access web interface using

**[http://localhost:8080/](http://localhost:8080)**.

with default login and password:
  * login: **Admin**  - just make sure you write uppercase *A* :-)
  * password: **zabbix**


# Advanced topics

### libvirt
You can run this machine using libvirt and KVM hypervisor. You need to install **libvirt** plugin for Vagrant first:
```
vagrant plugin install vagrant-libvirt
```

After that just launch machine using libvirt provider:

```
vagrant up --provider=libvirt
```

### Change ports
If you need to change ports on your host just edit Vagrantfile and replace *forwarded_port* stanza.
