:orphan:

.. _vcloud-automation-events:

========================
vCloud automation events
========================

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
