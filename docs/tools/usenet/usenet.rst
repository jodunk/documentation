Downloader
===========

+-------------------+--------------------+
| **Networking**                         |
+-------------------+--------------------+
| Hostname          | download           |
+-------------------+--------------------+
| IP                | 10.0.9.4           |
+-------------------+--------------------+
| Virtual Machine   | download           |
+-------------------+--------------------+
| Website           | http://10.0.9.4    |
+-------------------+--------------------+
| **Software**                           |
+-------------------+--------------------+
| OS                | Ubuntu 16.04.2 LTS |
+-------------------+--------------------+
| Last Updated      | May 2017           |
+-------------------+--------------------+
| **Hardware**                           |
+-------------------+--------------------+
| CPU               | 4                  |
+-------------------+--------------------+
| Memory            | 2GB                |
+-------------------+--------------------+
| Network           | DMZ                |
+-------------------+--------------------+
| Storage           | 100GB (SSD, thin)  |
+-------------------+--------------------+

A machine which uses Docker agents containing several different programs for downloading files.

Deploy
-------
This machine was set up using https://github.com/calvinbui/ansible-usenet-docker

Docker Containers
------------------
* NZBGet
* Sonarr
* Transmission
* NZB Hydra
* Sonarr
* CouchPotato

Certificates
-------------
Certificates are generated using Let's Encrypt on the host machine.

Folders
--------
Everything is based under ``/usenet``.

NFS Shares
-----------
The NFS share to HDD is under ``/usenet/hdd``.

This is configred in ``/etc/fstab``.

FreeNAS has allowed this by white-listing the IP (10.0.9.4).
