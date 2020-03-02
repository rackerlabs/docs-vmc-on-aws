:orphan:

.. _vcloud-vm-requirements:

===============
VM requirements
===============

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
