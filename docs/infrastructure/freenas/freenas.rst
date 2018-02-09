FreeNAS
=================

+-------------------+--------------------+
| **Networking**                         |
+-------------------+--------------------+
| Hostname          | freenas            |
+-------------------+--------------------+
| IP                | 10.0.X.5           |
+-------------------+--------------------+
| Virtual Machine   | freenas            |
+-------------------+--------------------+
| **Software**                           |
+-------------------+--------------------+
| Version           | FreeNAS 11.1       |
+-------------------+--------------------+
| Last Updated      | Feb 10 2018        |
+-------------------+--------------------+
| **Hardware**                           |
+-------------------+--------------------+
| CPU               | 4                  |
+-------------------+--------------------+
| Memory            | 16GB               |
+-------------------+--------------------+
| Network           | All                |
+-------------------+--------------------+
| Storage           | 8GB (mirror ZFS0/1)|
+-------------------+--------------------+
| PCI Device        | LSI2308            |
+-------------------+--------------------+

FreeNAS is the storage system holding everything together. It runs the **SSD** and **HDD** ZFS pools.

Pools
------

* Boot Drive: Mirrored (2x) on ZFS0 and ZFS1
* SSD: Mirrored (2x) 512GB Samsung 850 PRO

  * Mirror 0: da1p2 + da0p2

* HDD: Mirror (3x) in a stripe (RAID10)

  * Mirror 0: da5p2 + da4p2
  * Mirror 1: da7p2 + da6p2
  * Mirror 2: da3p2 + da2p2

Permissions
------------
All files and folders should be owned by "nobody:HOME\\Domain Users"

Access
-------

CIFS/SMB
^^^^^^^^^
Available at /files and /ssd on all network interfaces.

Access available to domain users.

Permissions are handled through Windows Security via Active Directory (home.net) using the freenas service account.

Workgroup is set to HOME (Domain) so no Domain is required.

FTP
^^^^^
Access available to root on port 21

NFS
^^^^^
Serving NFSv4

Restricted IP access.

SSD: /mnt/ssd - Only 10.0.0.3 is allowed (ESXi)
HDD: /mnt/hdd - 10.0.0.3 (ESXi) and 10.0.9.4 (Download)

Disks
---------
(Decrypt with OpenSSL)

.. code-block:: none

  U2FsdGVkX1/8pzLHffBOlyIiKO+H33t6KRGoSKp41DY2xA0yCFhPgFwH+lpuc9en
  1hQBuvjiI1xby0cZJ9CNS6o1gL4rqA1QYPZkULNPsNUPUfg+4BPl539Q1c40rvc5
  1t/BFiOI1iKzNn4xx3R6VNz84R1c6JTGnIMradReSFsbpzv8+RW5o1bcEUTNeFQI
  DGlHp/beSDY6vz+ZzTQKoOV3gfcfjVvdKr6jxCTYYWa+7e2JJAlsG5ONRNRaE0eO
  Y5R2pQ85Ror2EO94wuZZj2fOQOXAzWCBGiziRBG+VucaPVfz2HxMBN/94dmnfoWO
  JY7ufjlNHKltXUkKiTjk01foBGY6fUBZWGIHZhBmSBNj/uI7QG8uxmbpyBVeg9z0
  vLzU9pGZDyhaFmPCemgzV5/Nw9qW5BaBuar/c3ZMjntJ9C6D2wZUH/sA7ZeRdVqJ
  2Y0vrUAHNaF96GBN8eMW+Tr5RPNmyV04OWlzb0++FmI=

LSI 2308
---------
Currently installed: PH20.00.08.00-IT

SAS Address 000000000

Latest versions: ftp://ftp.supermicro.com/driver/sas/lsi/2308/Firmware/IT/

Boot into UEFI DOS Mode (built-in) and browse a connected USB to upgrade.
