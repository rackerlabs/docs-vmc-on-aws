.. _using:

================
Using RPC-VMware
================

This section describes the following Rackspace Private Cloud powered by
VMware (RPC-VMware) tasks:

-  :ref:`Accessing the RPC-VMware environment <rpcv-access>`

-  :ref:`Obtaining guest VM templates <rpcv-obtain-images>`

-  :ref:`Assigning public IP addresses <rpcv-assign-IPs>`

-  :ref:`Activating Rackspace-provided OS image licenses
   <rpcv-activate-image-license>`

-  :ref:`Patching the OS <rpcv-patch-os>`

-  :ref:`Managing capacity <rpcv-manage-capacity>`

-  :ref:`Using the API <rpcv-use-api>`

-  :ref:`Managing permissions <rpcv-manage-permissions>`

-  :ref:`Migrating workloads <rpcv-migrate-workloads>`

-  :ref:`Guest OS Clustering <rpcv-guest-os-clustering>`

-  :ref:`Using plug-ins and third-party software <rpcv-use-plug-ins>`

.. _rpcv-access:

Accessing the RPC-VMware environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For security reasons, you must establish a VPN connection to the
Rackspace firewall to access your RPC-VMware environment. You can
establish either a site-to-site or client-to-site VPN to satisfy this
requirement.

Your RPC-VMware environment includes DNS servers, which provide local
DNS resolution. Therefore, you must configure conditional forwarding
in your DNS infrastructure to correctly resolve DNS records
for RPC-VMware management services. Contact your support team for
more details.

Rackspace creates ticket with the details of how to establish a VPN connection
and how to access the various services in your RPC-VMware environment. If
you have purchased several environments in different data centers, you will
receive individual tickets specific to each environment.

.. _rpcv-obtain-images:

VM templates
~~~~~~~~~~~~~~~

Rackspace provides complimentary OS templates for deploying VMs. These OS
templates
use the vCenter Content Library system and are configured as a subscribed
third-party
library. If you request the subscription during or after your RPC-V
deployment, the OS
templates consume a small amount of disk space on one of the available
datastores in your RPC-V environment.

Rackspace will only provide complementary OS templates for operating systems
listed on the `EOL Terms <https://www.rackspace.com/information/legal/eolterms>`_
page that have not yet reached the End for Sale date. The Rackspace template
catalog is periodically updated to add or remove OS templates based on
their status on this page.

.. _rpcv-assign-IPs:

Assigning public IP addresses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Rackspace can provide public Internet Protocol (IP) addresses to assign to VMs
and other virtual systems that you deploy within your RPC-VMware environment.
Rackspace provides these public IP addresses by assigning small blocks of
IP addresses to the external interface of the physical firewall in your
environment and establishing NAT assignments to private IP addresses behind
the firewall. Rackspace works with you to determine how many public IP
addresses you require and which internal networks the NATs should be
assigned to. Rackspace provides you with a table listing this public IP NAT
assignment.

.. important::

   It is your responsibility to manage the assignment of private IP addresses
   that correspond to a public IP address. This ensures you are able to
   externally
   access any systems provisioned by you in your environment.

Rackspace can assist you in managing access rules on the physical firewall to
restrict unwanted access to a system with a public IP address enabled. You can
manage these access rules by using the My Rackspace portal. It is your
responsibility to remove or adjust these rules if a private IP address is no
longer used or transferred to a different virtual system.
If you need Rackspace assistance with the access rules on the
physical firewall, create a support ticket or call your dedicated account team.

If any additional IP addresses are required, contact your Rackspace Support
team.

.. _rpcv-activate-image-license:

Activating Rackspace-provided OS image licenses
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you purchase host-based OS licensing for Windows or Red Hat from Rackspace,
instructions on how to activate the licenses are provided by your account team.
Failure to follow these instructions might impact the function of the OS.

.. _rpcv-patch-os:

OS patching
~~~~~~~~~~~

You can manage your OS patches by using any external OS patching source
provided by the OS manufacturer. If you have purchased a host-based license
for Red Hat Enterprise Linux, you will receive instructions on how to use
the Rackspace OS patching sources for that OS, if you choose to use them.
If you encounter configuration issues or patching is not working, enter a
support ticket or call your dedicated account team.

.. _rpcv-manage-capacity:

Capacity management
~~~~~~~~~~~~~~~~~~~

You are responsible for capacity management and must inform Rackspace when
additional resources are required. You can use vCenter Server alarms and
performance graphs to monitor cluster, host, VM, and datastore resources.

To aid in capacity planning, we recommend using VMware vRealize Operations.
vRealize Operations has advanced forecasting, monitoring, and rightsizing
capabilities, including email alerts and Simple Network Management Protocol
(SNMP). The vRealize Operations dashboard enables you to best manage your
resources and optimize performance.

.. note::

   For capacity management, you can choose to use third-party software that is
   compatible with RPC-VMware services. However, Rackspace does not guarantee
   compatibility with third-party products, and functionality is limited within
   the Customer Access role permissions.

.. _rpcv-use-api:

Using the API
~~~~~~~~~~~~~

You can use the VMware APIs within the boundaries of the permission
set of each component that you purchase for RPC-VMware. For the most
up-to-date API information, see the
`VMware site <https://www.vmware.com/support/pubs/sdk_pubs.html>`_.

.. _rpcv-manage-permissions:

Managing permissions
~~~~~~~~~~~~~~~~~~~~

Rackspace retains administrative access to the RPC-VMware environment. However,
over 300 permissions are enabled so that you can manage the hosted VMs.

If you have a specific use case or third-party system that you want to
integrate with your RPC-VMware environment but can’t because of the level of
access provided to you, discuss your requirements
with your account team to determine adjustments can be made. Requests for
additional permissions are reviewed on a case-by-case basis. Create a ticket
or call your dedicated account team to discuss your requirements.

If you have selected to use the Rackspace-provided directory service
to host user accounts for your staff, create a ticket
to request additional user accounts or changes to existing accounts.

.. note::

   It is your responsibility to request user account deletion for staff no
   longer authorized to access your RPC-VMware environment.

If you have selected to use your internal Active Directory (AD) to host user
accounts for your staff, it is your responsibility to manage user accounts
that need to be added to or removed from groups that have been enabled for
various access roles in your RPC-VMware environment.

.. _rpcv-migrate-workloads:

Migrating workloads
~~~~~~~~~~~~~~~~~~~

Rackspace has two primary methods for migrating workloads:

* Network migration: Use for small data sets
* Physical migration: Use for large data sets

When choosing a method, you need to assess the time, cost, difficulty, amount
of data to be migrated, including any discussions with Rackspace before
making a selection on what method you choose to use.

VMs can be migrated in either a powered on or powered off state; however,
powered on migrations have specific requirements that must be met for
continuous operation. Powered off migrations have the most flexibility in
transfer options but require downtime for the services running on the VMs.

When selecting a migration method, note the following considerations:

-  Bandwidth and latency: Transfers over the network between sites can be
   affected by low bandwidth or latency, increasing the transfer time or
   preventing live VM migrations.

-  Timescale for the migration: The size of the VMs might not allow timely
   transfer over a network. A physical transfer using a USB drive (or similar
   method) might result in faster transfer times even with the added time
   of shipping the drive.

-  Downtime for the VMs: A physical transfer requires downtime. Some network
   methods allow continuous operation or minimal downtime.

-  Dataset size: Smaller VMs are more easily transferred over a network,
   while large amounts of data take time to transfer and might be better
   suited for physical transfer.

-  Longevity of the solution: Is the migration  temporary or permanent?
   You need to note which devices will need to be
   decommissioned, repurposed, or rebuilt.

-  Cost for the solution: The cost can range from free, with the customer
   performing all the work, to customer assistance,
   to Professional Services engagements, and depends on the complexity of
   the migration. Additional equipment, infrastructure, and licensing can
   also affect the cost.

-  Skill set of the customer: The self-service option might be sufficient for
   some customers, while others might need assistance from Professional
   Services.

-  Versions of the VMware products: Certain migration methods require
   specific versions of the VMware products to properly facilitate the
   migration.

-  Complexity of customer environment: More complex customer environments or
   business requirements might dictate a specific migration process.

-  Snapshots: We recommend removing any VM snapshots before migration to
   ensure disk file integrity.

Rackspace provides assistance in selecting, enabling, and even performing
the migration of your existing workload to your RPC-VMware environment.

Contact your dedicated account team to discuss the services and pricing.

.. _rpcv-guest-os-clustering:

Guest OS Clustering
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can run clustered instances of guest VMs in your RPC-VMware environment,
subject to the following configuration restrictions.

- Virtual machines participating in clustering must remain compatible with
  vMotion. This might require OS level configuration steps. Contact your
  support team for further details.
- Virtual machines participarting in clustering with a shared disk
  configuration must reside on external SAN storage. Rackspace can provide
  fully managed Dedicated or Shared SAN for this purpose.
- Windows VMs participating in clustering must run Windows 2008 SP2 or later.
- Rackspace Managed Backup for RPC-VMware is not currently available for
  clustered guest VMs.



If you are interested in running clustered guest OS services,
contact your support team for further details.

.. important::
   Rackspace must be able to place ESXi hosts into maintenance mode
   in order to patch your RPC-VMware environment. Any configuration
   that you create that prevents this may be removed. Speak to
   your support team for more details.

.. _rpcv-use-plug-ins:

Using plug-ins and third party software
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can use plug-ins and third-party software that operates with the Customer
Access permissions provided to you.

.. important::

   Rackspace does not guarantee compatibility with anything that you may
   install or configure with your RPC-VMware environment.

If Rackspace determines that a plug-in or third-party software tool is causing
reliability or stability issues with your RPC-VMware environment that affect
Rackspace’s ability to support and maintain it, we notify you and work
with you to resolve the issue.
