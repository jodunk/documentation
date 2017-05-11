Networking
===========

Ubuntu
-----------

``/etc/network/interfaces`` ::

 iface eth0 inet static
 address 10.0.9.6
 network 10.0.9.0
 netmask 255.255.255.0
 broadcast 10.0.9.255
 gateway 10.0.9.1
 dns-nameservers 10.0.9.1

 iface eth0 inet static
 address 10.0.0.6
 network 10.0.0.0
 netmask 255.255.254.0
 broadcast 10.0.1.255
 gateway 10.0.0.1
 dns-nameservers 10.0.0.1


CentOS
---------

``/etc/sysconfig/network-scripts/ifcfg-eth0`` ::

  DEVICE="eth0"
  ONBOOT=yes
  TYPE=Ethernet
  BOOTPROTO=static
  NAME="System eth0"
  IPADDR=10.0.0.9
  NETMASK=255.255.254.0
