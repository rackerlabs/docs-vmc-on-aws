:orphan:

=============
vApp networks
=============

vApp networks are isolated to a single vApp. They cannot span across
vApps unless it they connected to an organization network through a
routed or direct connection. If a vApp network is going to be a routed
network, a vShield Edge is automatically deployed to provude NAT
services when the vApp is powered on. When connected to a routed
network, a network pool is required. However, a vApp network does not
need to connect to an organization network, which enables an isolated
network.

.. image:: ../figures/vcloudnetworks-vAppnetworks.png
