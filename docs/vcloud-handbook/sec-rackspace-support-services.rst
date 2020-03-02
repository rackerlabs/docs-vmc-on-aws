.. _rackspace-support-services:

==========================
Rackspace support services
==========================

This section describes the following topics:

-  Support and automation services for Dedicated VMware vCloud
   environments

-  Supported VM types

-  VM requirements

-  vCloud automation events

Dedicated VMware vCloud services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Rackspace provides some specific support and automation services for the
Dedicated VMware vCloud environment and the virtual machines that are
built in it.

Infrastructure support
    Rackspace delivers Fanatical Experience™ for the hardware infrastructure
    resources including Network, Server and Storage components.

VMware virtualization services
    Rackspace is one of VMware's largest global vCloud Air Network
    partners, with elevated access to technical specialists for rapid
    resolution of unexpected software-related issues within the VMware
    stack.

    Rackspace's VMware Certified Professionals (VCPs) assist in the
    architecture, deployment and troubleshooting of the environment.
    Rackspace monitors and maintains the VMware software stack,
    including installing and configuring the vCloud, vCenter and vROps
    servers, backing up the VMware service VMs, and monitoring the
    hypervisors. Rackspace supports the vCloud and vCenter web UI, and
    APs.

Virtual machines
    Rackspace patches and monitors guest operating systems, backs up
    VMs, and installs and patches antivirus on VMs created from
    Rackspace Managed OS templates. Rackspace also provides support for
    Rackspace unmanaged or customer-provided virtual machine containers
    and their performance within the cloud. See `Virtual machine types`_
    and `VM requirements`_ for more information.

vCloud support automation
    Certain activities in vCloud trigger Rackspace automation. This
    allows Rackspace to populate information in the support systems for
    tracking, monitoring, and supporting VMs created in vCloud. See
    `vCloud automation events`_ for more information.

Virtual machine types
~~~~~~~~~~~~~~~~~~~~~

The following VM types can be included in vApps. See `VM requirements`_
for information about the features required for a vApp virtual machine.

Rackspace Managed
    Rackspace managed VMs are created from templates in the Rackspace
    Catalog designated as "Managed" and have Rackspace support services
    including for the guest OS. Since Rackspace supports the guest OS,
    we add services, user accounts, and OS modifications necessary for
    that managed service.

Rackspace Unmanaged
    Rackspace Unmanaged VMs are created from templates in the Rackspace
    Catalog designated as "Unmanaged" and do not have Rackspace guest OS
    support services. Rackspace does not support the guest OS; our
    support teams and automation services do not interact with the guest
    OS.

Customer provided
    Customer-provided VMs are created from templates that you upload to
    a catalog or you can directly upload virtual machines to vCloud.
    Rackspace does not support the guest OS; our support teams and
    automation services do not interact with the guest OS.

VM requirements
~~~~~~~~~~~~~~~

A new virtual machine must meet the following requirements:

**Networking**

 **Rackspace Managed VMs**: These VMs should have at least two NICs.
 Only one secondary NIC can be connected to a ServiceNet network.
 Connect all other NICs, including the primary NIC, to one of the
 ExNet networks.

 .. note::

    If you select a NIC to be the primary NIC, vCloud Director pushes
    the gateway and DNS settings to the network adapter of the Guest OS
    running in this virtual machine. No DNS or gateway settings are
    pushed to other NICs, since they are not the primary NIC. vCD only
    pushes the IP address and subnet to these other NICs.

 **All other VMs**: These VMs should have one or more NICs connected
 to the ExNet networks and cannot be connected to any ServiceNet
 networks. ServiceNet only supports Rackspace-managed VMs.

 **IP allocation**: Use the allocation type "Static - IP Pool". Using
 DHCP is not supported. Rackspace does not recommend using "Static
 Manual", since an incorrect IP entry causes our automation to fail.

 .. warning::

    Since the firewall is configured to deny access by default, add ACL
    rules to allow inbound access to the new VM. Otherwise, our
    automation generates a ticket when the VM is initially powered on,
    requesting that the network configuration be corrected before
    support automation can continue.

    Rackspace automation assigns a public IP address for every private
    IP address assigned to the VM and creates NAT rules on the firewall
    to allow external communication. The firewall is configured to deny
    access by default. To allow inbound access, add appropriate ACL
    rules.

**Advanced vCloud networking**: Rackspace does not support the use
of advanced networking features such as routed, isolated, or fenced
vApp networks. All VM network connections must be made directly to
the Rackspace-provided external networks.

**Virtual machine name**

 .. warning::

    Special characters in a VM name are automatically removed by our
    automation, leaving only the remaining allowed characters. The name
    field is restricted to 128 characters.

 Rackspace VM names are created in accordance with the following standards:

 - The original VM name is stored as the device nickname in the
   MyRackspace portal.

 - A six digit number followed by a "-" (hyphen) is added to the
   beginning of the VM name. This number is used by our support
   team.

 - The first eight characters of a Windows VM or the first 55
   characters of a Linux VM computer name entered in vCloud are used
   for the next portion of the VM name.

 - A default domain name taken from email of the primary contact
   name at your company is added to the name of the VM.

 - No special characters other than "-" (hyphen) and "." (period)
   are allowed in the VM container name. (See VMware KB: `VMware
   Base <http://kb.vmware.com/kb/2046088>`__). Special
   characters are automatically removed.

**Computer Name**

 If guest customization is enabled, the Computer Name field in vCloud
 is used to set the host name in the guest OS. The name is subject to
 the following limitations:

 - This field is restricted to 15 characters for Windows. For
    non-Windows systems, it is restricted to 63 characters and can
    contain dots.

 - Alphanumeric characters and hyphens are allowed. The name must
    not contain only digits.

 For Managed VMs, only the support system 6 digit device number and a
 "-" (hyphen) is prepended to the Computer Name. This may truncate
 the original name to meet the character length limitations.

 For example, if a new VM is created with the VM Name ``App1VM`` and
 the Computer Name ``app1``, the resulting name for the Rackspace
 Managed VM is ``123456-app1.domain.com`` for a Linux VM and
 ``123456-app1`` for a Windows VM. The original ``App1VM`` VM name is
 listed as the alias for ``123456-app1.domain.com`` in the
 MyRackspace portal.

**Passwords**

 .. warning::

    Do not change the default password settings on the Guest OS
    Customization page.

 All vCloud VMs use the administrator or root password set by vCloud
 guest customization as displayed in the VM properties.

 .. image:: ../figures/guest-os-customization.png

vCloud automation events
~~~~~~~~~~~~~~~~~~~~~~~~

The following vCloud events trigger Rackspace automation:

Building a new VM
    Rackspace automation is triggered when a VM is initially powered on.
    Dedicated VMware vCloud environments interact with Rackspace
    back-end automation and support systems, putting limitations and
    requirements on the type of VM that is built.

    After a new virtual machine is powered on, a ticket is produced to
    notify the user that an automation process started. Do not log in
    to, make modifications to, or power cycle the VM until you receive a
    ticket indicating that this process is complete. Only make
    modifications to the VM if a ticket from Rackspace explicitly
    requests a modification.

    If Rackspace automation experiences any issues registering a new VM
    with our support systems or adding the public IP or NAT assignments
    to the firewall, we are immediately notified of the issue. If there
    are delays in processing the new VM, Rackspace issues a notification
    ticket.

    For Rackspace-managed VMs, Rackspace automation logs in to the VM to
    configure monitoring, patching, and backup services in accordance
    with the Rackspace support system. All accounts have default
    settings for these services. To change settings, contact the support
    team after the automation is complete.

Modifying a VM
    Rackspace automation is triggered if VM attributes change. This
    keeps Rackspace systems up to date with the properties of the VM. Do
    not change the computer name for a Rackspace-managed VM. Also, the
    virtual machine name for any VM should not be changed, since
    Rackspace tracks the virtual machine by name in your environment. If
    the name is changed, Rackspace automation rewrites the name to its
    former value. To change either of these names, contact your account
    team for assistance.

Changing the power state of a VM
    When a VM is powered on or off, suspended, or resumed after
    suspending, Rackspace adjusts the monitoring systems so that the
    user does not receive alerts for a VM that is intentionally shut
    down. Our automation also suspends usage for VMs that are powered
    off. Suspended VMs do not qualify for usage suspension.

Deleting a VM
    If a VM is deleted, Rackspace automation removes references to that
    VM from Rackspace support systems and makes the local IP assigned to
    the deleted VM available for reuse. The Rackspace automation process
    does not remove or alter any ACLs created for those IPs. Since a new
    VM can receive the local or public IP of a deleted VM, use the
    MyRackspace portal to remove all associated physical firewall ACLs
    associated with the deleted VM.
