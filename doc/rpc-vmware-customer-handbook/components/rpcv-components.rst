.. _rpcv-components:

=====================
RPC-VMware components
=====================

RPC-VMware is composed of one or more dedicated VMware vSphere cluster managed
by a dedicated vCenter Server. RPC-VMware provides core components and,
optionally, one or more add-on components. The core components and some
of the optional add-on components require management services, such as
vCenter Server, Platform Services Controller (PSC), and NSX Manager. These
must run in the same cluster as your workloads. The services must
always have access to sufficient compute resources or the RPC-VMware
functionality and availability will be at risk. To address this requirement,
the management services run
in a designated cluster resource pool, which guarantees access to sufficient
resources. The management services can consume more compute resources in the
future as VMware releases newer versions of their software.

Rackspace manages and maintains the RPC-VMware product’s VMware
services and infrastructure resources. Any changes to settings or
configurations of the VMware-hosted services, networking, storage, and compute
systems must be requested by opening a ticket with Rackspace Support.

You can view and manage your virtual systems that you provision
from the RPC-VMware services user interfaces (UIs) and APIs.

The following table describes the management services for the core components
of RPC-VMware. Your private cloud includes these services.

**Management services for core components**

.. list-table::
   :widths: 30 70
   :header-rows: 1

   * - Service
     - Description
   * - Management resource pool
     - A cluster resource pool where the required and optional management
       services reside. The resource pool is used to restrict access and to
       manage resources for the management services. The resource pool and the
       VMs running in it are required and are managed by Rackspace. Management
       services, such as VMware vCenter Server and the PSC, are requirements
       for providing and managing
       RPC-VMware. These services must always have access to sufficient
       compute resources or the RPC-VMware functionality and availability is
       at risk. To address this requirement, the resource pool is
       configured to reserve a sufficient amount of CPU and memory resources.
       The amount of reserved resources could be increased in the future as
       VMware releases newer versions of their software.
   * - Management network
     - A single VLAN segment behind your firewall exclusively used for
       the management of RPC-VMware. Rackspace requires network access to
       management services and infrastructure for monitoring, troubleshooting
       and resolution of issues. The customer and Rackspace co-manage the
       firewall rules.

       .. important::

          Do not modify the firewall rule set in a manner that prevents
          Rackspace from accessing the management network and infrastructure
          as you can negatively impact the Service Level Agreement (SLA). If
          you do interrupt Rackspace network access by a change to
          firewall rules, Rackspace reverts or alters the customer created
          firewall rules and contacts you about the change. This is
          required due to VMware license reporting requirements for your environment.

   * - vCenter Server virtual appliance
     - Provides centralized visibility, proactive management, and extensibility
       for VMware vSphere from a single console. vCenter Server is accessible
       from the vSphere client and the vSphere API.
   * - PSC virtual appliances
     - Provide identity management for users and applications that interact
       with VMware vSphere and licensing services to RPC-VMware.
       The PSC is paired directly with the
       vCenter Server, and as such, does not require a separate management
       interface.
   * - NSX® Manager virtual appliance
     - The NSX Manager provides the graphical user interface (GUI) and the REST
       APIs for creating, configuring, and monitoring virtual network
       components.
   * - Virtual Machine Recovery (VMR) virtual appliance
     - Enables image-based backup of the management services. It allows
       Rackspace to quickly recover management services. This VMR appliance
       is for use only by Rackspace and does not back up any of the VMs created
       by the customer on the compute cluster. No customer access is provided
       to the VMR appliance.
   * - Jump server
     - Rackspace uses this system to gain access into your cluster to maintain
       the management services. No customer access is provided.
   * - vRealize® Operations Manager™ virtual appliance
     - The vRealize Operations Manager virtual appliance provides all
       vRealize Operations Manager functionality, enabling activities
       such as checking the health of the hosted VMware environment,
       performing capacity planning, and proactively eliminating performance
       bottlenecks. It is accessible via a web interface.
   * - vRealize Log Insight virtual appliance cluster
     - Rackspace uses this system to monitor the management services of
       RPC-VMware. No customer access is provided. However, log message
       forwarding can be configured on request. Contact your Support
       team for more details.
   * - SDDC Manager virtual appliance
     - Provides orchestration services for the administration of RPC-VMware.
       This
       is consumed by Rackspace. No customer access is provided.
   * - DNS servers
     - Provide local DNS resolution for the management components of RPC-
       VMware.
       No customer access is provided.
