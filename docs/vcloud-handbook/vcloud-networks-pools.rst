:orphan:

=============
Network pools
=============

A network pool is a group of network resources that can only be used by
a vCloud Organization. These can be either logical or physical
networking resources.

The network pool shares the IP address pool with organization and vApp
networks for NAT routing. vCloud supports three types of network pools
that can be used by vApps.

 Port-group backed
    Port-group backed pools require pre-created port-groups within the
    vSphere environment. Port-group backed pools do not require vDS and
    can be based on vSS, vDS or Cisco Nexus 1000v.

    Rackspace uses a port-group backed layer 2 network, which enables
    autonomous control of the network resources and ease of
    configuration.

 VLAN backed
    VLAN-backed network pools require a set of unused VLANs. When an Org
    or vApp network based on a VLAN-backed pool is created, a port-group
    is created on a dvSwitch and a VLAN is assigned to this port-group.

 vCD-NI backed
    vCloud Network Isolation-backed (VCNI) network pools are flexible,
    easy to configure and do not require VLANs. vCNI provides layer 2
    isolation by utilizing a network overlay. This network overlay is
    provided by MAC in MAC encapsulation and requires a vDS. For each
    consumed network vCloud Director creates a port-group and assigns
    this port-group a network ID number. This network ID number is used
    for the encapsulation of the traffic.

    Because vCD uses MAC in MAC for the encapsulation of traffic, vCD-NI
    requires an increase in the MTU of the underlying transport network
    (dvSwitch). This avoids frame fragmentation caused by the minor
    overhead in MAC encapsulation.

..  note::

    Rackspace Support Item: To ensure that Rackspace automation and support
    services have time to properly decommission the IP address associated
    with a deleted VM from our systems, Rackspace will set the IP address
    release timeout to 24 hours. A longer timeout can be requested, but a
    timeout cannot be requested less than the Rackspace default.

..  note::

    Rackspace Support Item: Port-group backed is the only network pool type
    available in Dedicated vCloud at this time. Rackspace is working to
    provide more advanced network functionality with NSX integration for
    vCloud.
