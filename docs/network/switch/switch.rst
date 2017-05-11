Switch
=======

+-------------------+--------------------+
| **Networking**                         |
+-------------------+--------------------+
| Hostname          | switch             |
+-------------------+--------------------+
| IP                | 10.0.0.2           |
+-------------------+--------------------+
| Website           | https://10.0.0.2/  |
+-------------------+--------------------+
| **Software**                           |
+-------------------+--------------------+
| Version           | 1.10.016           |
+-------------------+--------------------+
| Last Updated      | July 2015          |
+-------------------+--------------------+

D-Link DGS-1100-16 EasySmart Switch

Warranty
---------
Limited Lifetime Warranty. This means the warranty will only end five years after D-Link (or its successor) discontinues sales of the product in Europe. You must register your product to get the Limited Lifetime Warranty (see below).

(Decrypt with OpenSSL)

.. code-block:: none

  U2FsdGVkX19kOjKpDShVuMhrHUj5X9fJUpaL4ovP/gxQQ2oR48AazozkfaLU9JCQ
  eYn0d/YzUJDx901isGXo2Q1VpwJpCoKFj8PnAQEzqdZMzf2wsebzHIf9G7HpXMPB
  Lw6cpcgXgzzWngGkFSmkzREEHb/qo7gB5Ww/TDiLhEkK8nxIb/6WOVZ6REZpTAgB
  lNLRO+ROAMgxfcfcNl7+cuQjmlNnOOqDim0Ejhif4Ev1Jbkeg+ecgyVa5nIWo5eM
  vX9t/aEGFuyTBFaeRTiZAj/yEc0dIkbb6Ct+40ZNvhTlY2Q2Y0/bNODUi0dDpPde
  NMi95w8A+R1/htsm8tND51u1I997We1Cxlva+wetlx812fat7s669l/6bYgMiBOg
  3BAO9WoSWk91nSIRpVq+9QslTreggR/YB3YOamAmnUYb/v4QLfXY6r+dDVtFcd5r
  bwNlBMHLBbyYrsPFG49YV13QR0VP0Ua7ERlioEThA55FQPeL6kfU5vX3lWwMBDPY
  LCDVTKOj7vKMDCESM6Fr94qa3TODEQq2xQZau30S3IunYL+MfrM/AXZCYXXrvET9
  cK87vDkvtYOgTsMho8UbUO7WLqyWRXL4mPN0qhce+jFBcyXeiLAR5+8x1hIsyQAg
  r/ojOHZ0unWSoInIPG2vyqtE57bemKAC3SGyIo+AT9hCGQpjpFbk9o3vQt+Vp0nk
  tbA3o1JyPvOlprSX4vi9vSuWfcHmFZV+GTDi9Nsch8M=

Port Trunking
--------------
Port 1,2,3,4 are in a trunk group

IEEE 802.1Q VLAN
-----------------

10 is Management VLAN (Admin)

999 is LAN

+-----+---------------+-------------+
| VID | Untagged      | Tagged      |
+-----+---------------+-------------+
| 1   | None          | None        |
+-----+---------------+-------------+
| 10  | 1 to 12       | 13-16       |
+-----+---------------+-------------+
| 20  | None          | 12-16       |
+-----+---------------+-------------+
| 999 | None          | None        |
+-----+---------------+-------------+

Configuration and Firmware Backups
-------------------------------------
https://github.com/calvinbui/documentation/tree/master/docs/network/switch
