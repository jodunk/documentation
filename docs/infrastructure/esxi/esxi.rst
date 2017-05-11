ESXi
====

+-------------------+--------------------+
| **Networking**                         |
+-------------------+--------------------+
| Hostname          | esxi               |
+-------------------+--------------------+
| IP                | 10.0.0.3           |
+-------------------+--------------------+
| Website           | https://10.0.0.3   |
+-------------------+--------------------+
| **Software**                           |
+-------------------+--------------------+
| Version           | 6.5d               |
+-------------------+--------------------+
| Last Updated      | May 2017           |
+-------------------+--------------------+
| **Hardware**                           |
+-------------------+--------------------+
| CPU               | E3-1230v3          |
+-------------------+--------------------+
| Memory            | 32GB DDR3          |
+-------------------+--------------------+

Currently installed on a 16GB Cruzer Blade (mpx.vmhba32:C0:T0:L0)

Update ESXi
-----------
`Go here <https://esxi-patches.v-front.de/>`_ and click on the latest Imageprofile

Licenses
-----------
ESXi 6.0 FREE License from VMware, works with 6.5

(Decrypt with OpenSSL)

``U2FsdGVkX1/7Sozs6M4f650PqfEPMSXY4ts26Cir8D4lA3rPMm9LiQXNetw9yqNX``

vSwitchs
-----------

vSwitch 0
^^^^^^^^^^^

.. image:: /infrastructure/esxi/vswitch0.png

* All port groups are set to **Route Based on IP Hash**

vSwitch 1
^^^^^^^^^^^

.. image:: /infrastructure/esxi/vswitch1.png

vSwitch 2
^^^^^^^^^^^

.. image:: /infrastructure/esxi/vswitch2.png

vSwitch 3
^^^^^^^^^^^

.. image:: /infrastructure/esxi/vswitch3.png

Storage
--------
* HDD (10.0.0.5:/mnt/hdd)
* SSD (10.0.0.5:/mnt/ssd)
* RECORDING
* ZFS0 - dc, pfsense and freenas main drive
* ZFS1 - dc, pfsense and freenas mirrored

VM Startup and Shutdown
------------------------
1. dc
2. pfsense
3. freenas (180 seconds)
4. ups
5. vms
6. the rest
