Domain Controller
=================

+-------------------+--------------------+
| **Networking**                         |
+-------------------+--------------------+
| Hostname          | home.net           |
+-------------------+--------------------+
| IP                |10.0.0.16/10.0.9.10 |
+-------------------+--------------------+
| Virtual Machine   | dc                 |
+-------------------+--------------------+
| **Software**                           |
+-------------------+--------------------+
| OS                | Windows 2012 R2    |
+-------------------+--------------------+
| Last Updated      | July 2015          |
+-------------------+--------------------+
| **Hardware**                           |
+-------------------+--------------------+
| CPU               | 4                  |
+-------------------+--------------------+
| Memory            | 2GB                |
+-------------------+--------------------+
| Network           | Admin + DMZ        |
+-------------------+--------------------+
| Storage           |41GB (mirror ZFS0/1)|
+-------------------+--------------------+

Domain Controller, Active Directory, RADIUS server, Certificate Authority and DNS.

Domain
------------------
Runs the ``home.net`` domain

Active Directory (AD DS)
------------------------
Users are broken into two categories: Real and Fake

``CN=Real,CN=Users,DC=home,DC=net``

Runs on port 389 and 636 (SSL)

* User naming attribute: samAccountName
* Group naming attribute: cn
* Group member attribute: memberOf

DNS
----
Currently forwards to 10.0.0.1 (ADDS Properties -> Forwarders)


RADIUS (Network Policy Server - NPS)
--------------------------------------
Current RADIUS clients: 10.0.0.7

Policies

* Network policy grants access to people in the 'HOME\People' group
* Connection Request policy is for 'Wireless - Other OR Wireless - IEEE 802.11'

Security

* Microsoft: Protected EAP (PEAP)

Certificate Authority (AD CS)
------------------------------
Required for LDAPS

CA Certificate

.. code-block:: none

  -----BEGIN CERTIFICATE-----
  MIIDXzCCAkegAwIBAgIQH0J+6HSqh7RHJJa5uKLJCjANBgkqhkiG9w0BAQUFADBC
  MRMwEQYKCZImiZPyLGQBGRYDbmV0MRQwEgYKCZImiZPyLGQBGRYEaG9tZTEVMBMG
  A1UEAxMMaG9tZS1BRERTLUNBMB4XDTE0MTAwOTA3MzI0M1oXDTM5MTAwOTA3NDI0
  M1owQjETMBEGCgmSJomT8ixkARkWA25ldDEUMBIGCgmSJomT8ixkARkWBGhvbWUx
  FTATBgNVBAMTDGhvbWUtQUREUy1DQTCCASIwDQYJKoZIhvcNAQEBBQADggEPADCC
  AQoCggEBAJ5HigUI49W7X402s5XH4vsC+UBkaxqKqL+OFbRKtf3lmmTas6/ZEgE9
  MuXYdsCOL3U/jjTZfXRe4KEHTbWEgFWiBIZ6hg25RbTKzRv6c4n/CdIToI09Ec8F
  4cLHvV0C5Se0MiP/7X5KQtzXIdyy6KS1p87wEqYe3nFaigZRTgx+QVSGskHMIJeO
  ttLSV3k7EDMj+HeQaGZkIMMBguzr56Gbyl2oxY+V3lggfAs1IYVk/X6U0JP1dMTC
  5ffOqjKSFTtxbbb47S4qzPaY7/H/LCVxObZ4ab/yW4VgOd0C5I+T25udBpa8psXj
  FQQ7Qm9WjnvnjKywLu9Yr6HfDNG3y6UCAwEAAaNRME8wCwYDVR0PBAQDAgGGMA8G
  A1UdEwEB/wQFMAMBAf8wHQYDVR0OBBYEFPrFTh+nx6zgECM/h00YyIT67ZKAMBAG
  CSsGAQQBgjcVAQQDAgEAMA0GCSqGSIb3DQEBBQUAA4IBAQADHHr2PBNAfFnBD0Y9
  xdIvRXIfC19RDGMgRgvaTE8q8Z270+Cp4hJvbdEB0wJzCy551SYTbmn3CU/FoJFH
  z92h45ULZkF76XjEFp3B4ialpYiVVLc0tQUW799afGeRSWGvdwqvkb3FyQq5gTKH
  eWSnngKlWI4wOj+Rlyxje/+Cu9SZrWmlbiRZo228JZb9cTdkxt1b6evJjZoJcF49
  l/UYFBwnmzkQzVBxNP7prrC7jDxXbHs3NfGY+8wzCKqdTYGJG9BioNAdWFIV5JwL
  8FVx2OgTujk0yRMku1sUVG3ASfJG7SvtoFoRHxntHr3PxbZk6H/zMTDfIwKRMdqw
  RC+d
  -----END CERTIFICATE-----

CA Decrypted Private Key (Decrypt with OpenSSL)

.. code-block:: none

  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
