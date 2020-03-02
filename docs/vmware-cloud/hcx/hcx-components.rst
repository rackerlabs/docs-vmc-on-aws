==============
HCX components
==============

HCX is initially deployed as a virtual appliance, along with a vCenter plug-in
that enables the HCX feature. After the HCX Manager virtual appliance is
deployed, it is responsible for deploying the other appliances required for
HCX.
Mirror appliances are deployed at both the source and target locations. These
deployments provide the capabilities outlined below.

HCX Manager
~~~~~~~~~~~

HCX Manager provides a framework for deploying the service appliances. The
integration with vCenter allows HCX Operators to be authenticated, and allows
tasks to be authorized by using the existing SSO identity sources. Hybridity
actions can be initiated from the HCX Manager via the HCX User Interface in
vCenter and via virtual machine and distributed port group context menus.

HCX Interconnect
~~~~~~~~~~~~~~~~

The HCX Interconnect service appliance provides replication and vMotion based
migration capabilities over the Internet and private lines to the target site.
The interconnect provides encryption, traffic engineering, and virtual machine
mobility.


HCX WAN Optimization
~~~~~~~~~~~~~~~~~~~~

The HCX WAN Optimization service improves performance characteristics of the
VPN
or Internet paths by applying WAN optimization techniques like data
de-duplication and line conditioning. It accelerates onboarding to the cloud
using Internet/VPN, without waiting for Direct Connect/MPLS circuits.

HCX Network Extension
~~~~~~~~~~~~~~~~~~~~~

The HCX Network Extension service provides a Layer 2 extension
capability. The extension service permits keeping the same IP and MAC addresses
during a Virtual Machine migration. Network Extension with Proximity Routing
enabled ensures that forwarding between virtual machines connected to extended
and routed networks, both on-premises and in the cloud, is symmetrical.
