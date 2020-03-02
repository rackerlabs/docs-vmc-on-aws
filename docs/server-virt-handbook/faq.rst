==========================
Frequently asked questions
==========================

:Q: Do I get API access to the VMware vCenters?
:A: You do not have API access with VMware Server Virtualization.

    If this is of concern, contact your account manager to discuss
    your requirements. Your account manager can work with the VMware
    specialist team to potentially identify a solution.

:Q: Can I log in to the hypervisor?
:A: You cannot log in directly to the hypervisor. If you need to access your
    hypervisor, investigate `Rackspace Private Cloud powered by
    VMware <https://www.rackspace.com/vmware/private-cloud/>`_.

:Q: Are there standard resource allocation recommendations?
:A: It is important to size VMs as close to what is required as possible as
    resources like CPU, memory, and disk can be easily added but removal
    requires a restart and results in downtime.

:Q: Why does Rackspace reserve a percentage of storage for datastore overhead?
:A: Rackspace reserves a percentage of storage to ensure optimal performance
    and uptime of your environment. This is also used to perform functions like
    cloning, snapshotting, vSwap, and vMotion.

    For more information around the datestore overhead, consult your account
    team.

:Q: Can I suspend billing on VMs that are not in use?
:A: You have the ability to suspend the utility billing of virtual machines
    when they are not in use by powering down VMs through the MyRackspace
    portal. To power down VMs through the portal, see :ref:`Powering a virtual
    machine on and off <svh-power-vm>`.

         .. warning::

            By powering off a VM from within the OS you will not only generate
            an alert ticket for support to investigate, but the VM will continue
            billing at the daily utility rate.. To properly power off a VM and
            suspend billing, power off from the MyRackspace portal using these
            steps :ref:`Powering a virtual machine on and off <svh-power-vm>`.

:Q: Do I have access to the VM console?
:A: You do not have access to the console, but can access your VMs via
    SSH/RDP. If you have a need for VM console you access should investigate
    `Rackspace Private Cloud powered by VMware
    <https://www.rackspace.com/vmware/private-cloud/>`_.
