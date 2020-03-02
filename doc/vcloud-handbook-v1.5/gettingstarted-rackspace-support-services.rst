==========================
Rackspace support services
==========================

This section describes the following topics:

- Support for Dedicated vCloud environments

- Supported VM types

Dedicated vCloud services
~~~~~~~~~~~~~~~~~~~~~~~~~

Rackspace provides specific support for the Dedicated vCloud environment
and the virtual machines that are built in it.

Infrastructure support
 Rackspace delivers Fanatical Experience™ for the hardware infrastructure
 resources including Network, Server and Storage components.

VMware virtualization services
 Rackspace is one of VMware's largest global vCloud Air Network
 partners, with elevated access to technical specialists for rapid
 resolution of unexpected software-related issues within the VMware
 stack.

 Rackspace will assist in the architecture, deployment and
 troubleshooting of the environment. Rackspace monitors and maintains
 the VMware software stack, including installing and configuring the
 vCloud Director, vCenter Server and vRealize Operations servers,
 backing up the VMware service VMs, and monitoring the hypervisors.
 Rackspace supports the vCloud Director, vCenter Server, and vRealize
 Operations web portals, and APIs. Rackspace also provides support
 for virtual machine containers created from Rackspace-provided
 templates or customer-provided templates or vApps and their
 performance within Dedicated vCloud.

Virtual machines
 The customer is responsible for guest operating systems, backing up
 VMs, and installing antivirus, and patching VMs created from
 Rackspace OS templates. See :ref:`virtual_machine_types` and
 :ref:`vm_requirements` for more information.

.. _virtual_machine_types:

Virtual machine types
~~~~~~~~~~~~~~~~~~~~~

The following VM types can be included in vApps. See :ref:`vm_requirements`
for information about the features required for a vApp virtual machine.

Rackspace Templates
 Rackspace provides a catalog of courtesy templates. These templates
 have a base OS installation and are not maintained or patched. You
 can create VMs from these templates, but Rackspace does not support
 the guest OS. Rackspace support teams and automation services do not
 interact with the guest OS.

Customer provided
 Customer-provided VMs are created from templates that you upload to
 a catalog or you can directly upload virtual machines to Dedicated
 vCloud. Rackspace does not support the guest OS; our support teams
 and automation services do not interact with the guest OS.

.. _vm_requirements:

VM requirements
~~~~~~~~~~~~~~~

A new virtual machine must meet the following requirements:

Networking
 **IP allocation**: You are responsible for tracking the IP
 allocation in your environment and correlating the CSV file that has
 been provided to you to determine the public IP address for any
 private IP address allocated.

 .. warning::
    Since the firewall is configured to deny access by default, add ACL
    rules to allow inbound access to the new VM.

    **vCloud Director advanced networking**: Rackspace does not support
    the use of advanced networking features such as routed, isolated, or
    fenced vApp networks in Dedicated vCloud. All VM network connections
    must be made directly to the Rackspace-provided external networks.

Passwords
 All Dedicated vCloud VMs can use the administrator or root password
 set by using guest customization as displayed in the VM properties.

Storage
 While storage policies are used to abstract the placement of virtual
 machine disks onto specific datastores, it is important to note that
 there are certain limitations that apply to vApps and virtual
 machine disk files. An entire vApp including all virtual machines
 and their virtual disk files must all be contained within the same
 datastore for a selected Storage Policy. Thus the largest available
 free space of any given datastore within a storage policy becomes
 the current limit to the size of vApp that can be provisioned.
