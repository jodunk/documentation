How to configure pfSense as multi wan (DUAL WAN) load balance failover router
=============================================================================

How do I setup a multi-WAN load balancing and failover on pfSense router with two ADSL or cable or leased-line or FTTH (Fiber to the home) connections?


In this tutorial you will learn how to configure pfSense to load balance and fail over traffic from a LAN to multiple Internet connections (WANs) i.e. dual wan.

Why and how to setup a dual wan router?
---------------------------------------

A dual wan setup allows you to increase your internet bandwidth. You can load balance traffic as per your needs. You can get internet connection redundancy and failover. If one connection goes down your traffic will be routed automatically to a backup connection.

Requirements
------------

Two internet connections from two different ISPs. You can mix-match ADSL/FTTH/4G LTE/Cable/T1/FIOS connection as per your needs.

1. pfSense router with three network ports (NICS).
2. Two ISP modems with network port (NIC)
3. Static or dynamic IPs from ISPs
4. Monitor IP # 1 for ISP # 1 – 8.8.8.8 (google dns IP)
5. Monitor IP # 2 for ISP # 2 – 208.69.38.205 (opendns IP)
