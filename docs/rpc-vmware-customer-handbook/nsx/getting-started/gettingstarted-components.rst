
NSX components
--------------

The following table describes each component of NSX for RPC-VMware.

.. list-table::
   :widths: 20 10 70
   :header-rows: 1

   * - Component
     - Count
     - Description
   * - NSX Manager
     - 1
     - Provides an aggregated system view and is the centralized network
       management component of NSX. NSX Manager is installed as a virtual
       appliance on any ESXi host in your vCenter environment.
   * - NSX Controller
     - 3
     - The central control point for all logical switches within a network.
       Controllers maintain information about all VMs, hosts, logical
       switches, and VXLANs.
   * - VTEP
     - NA
     - Every ESXi host enabled for NSX is configured with an additional
       VMkernel port used as a VXLAN Tunnel End Point (VTEP). In other words, a
       VTEP is a host interface that forwards Ethernet frames from a virtual
       network via VXLAN or vice-versa.
   * - VXLAN
     - NA
     - Virtual Extensible LAN (VXLAN) is a encapsulation protocol for running
       an overlay network on existing layer 3 infrastructure. An overlay
       network is a virtual network that is built on top of existing network
       layer 2 and layer 3 technologies to support software defined networks.
