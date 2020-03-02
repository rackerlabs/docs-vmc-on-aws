:orphan:

.. _vcloud-vm-types:

=====================
Virtual machine types
=====================

The following VM types can be included in vApps. See
:ref:`vcloud-vm-requirements` for information about the features required
for a vApp virtual machine.

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
