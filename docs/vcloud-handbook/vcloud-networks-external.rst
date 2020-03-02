:orphan:

=================
External networks
=================

External networks are the foundation of organization networks. If the
organization network must access a corporate network or the internet, it
will move along an external network. Configuring an external network
requires preconfiguration in vCenter and for all hosts to have access to
the new port group. Once this is completed, the external network can be
added to vCD.

.. image:: ../figures/vcloudnetworks-externalnetworks.png

Setting up an external network requires the following layer 3
information:

-  Gateway

-  Subnet mask

-  DNS address

-  IP address

This information is abstracted from the end user, and used to provide
VMs with direct connection to the external network. The pool of IP
addresses is reserved for use only with vCD.

.. warning::

   If these addresses are not reserved and are used outside of vCD, network
   conflicts will occur.
