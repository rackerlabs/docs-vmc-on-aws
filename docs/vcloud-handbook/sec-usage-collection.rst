================
Usage collection
================

Virtual machines that are powered on or suspended have usage captured
for the time they are in that state. Daily usage events are sent at
midnight UTC for each server that exists at that time.

An additional usage event is captured when the following events occur:

-  A VM is resized (vCPU or vRAM changes)

-  Guest OS support is added or removed

-  An application license is added or removed

-  Application support is added or removed

-  The server is shut down or suspended

A server is not charged for time when the server is shut down. A server
is charged upon restart.

 Suspended VMs
    All virtual machines in a powered on or suspended state will incur
    usage during the power on period. If a virtual machine is powered
    off, usage is not collected or billed.

 Test VMs
    During the implementation process, Rackspace will create and power
    on a virtual machine to test that the environment is properly
    configured and to ensure connectivity with Rackspace internal
    systems that are required for provisioning virtual Machines. This
    test virtual machine is tagged to identify it, ensuring that the
    account is not billed for the usage during our testing. A record for
    a testing virtual machine shows an inactive and decommissioned
    status in vCloud and in the MyRackspace portal.

    .. note::

       During testing, ticket notifications showing status of the new
       virtual machine are displayed.
