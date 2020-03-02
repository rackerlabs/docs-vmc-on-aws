=========================
Managing virtual machines
=========================

This section details the functionality available in the MyRackspace
Portal for your VMware Server Virtualization components. This includes
virtual machine self-service and order tracking.

.. important::

   Before you begin, ensure that you are on the ``Dedicated Hosting`` tab on
   the top right-hand corner of your browser.

   ``Dedicated Hosting`` is highlighted in red if you are in the
   correct tab.

.. _svh-power-vm:

Powering a virtual machine on and off
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following steps to power a virtual machine on and off:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The Virtual Machines
   management section displays.

#. Select the virtual machine that you want to clone from the virtual machine
   list. This action opens up your individual virtual machine's details.

#. Click the ``Actions`` dropdown menu on the right-hand side.

#. In the ``Automate Action`` section, select ``Power VM...``.

#. If you select power off, the action powers down the selected virtual
   machine and suspends billing.

   If you select power on, the action powers up a previously off
   virtual machine and initiates billing.

   .. note::

      If you are powering on a virtual machine again, this might require
      review from a Rackspace VMware Support technician. For best practice and
      security reasons, OS updates might need to be applied before the virtual
      machine is returned to service, depending upon the length of time the
      virtual machine has been powered off. A ticket generates with this
      request and the Rackspace VMware Support team updates the ticket
      accordingly.

Rebooting a virtual machine
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following steps to reboot a virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The Virtual Machines
   management section displays.

#. Select the virtual machine you want to clone from the virtual machine list.
   This action opens up your individual virtual machine's details.

#. Click the ``Actions`` drop-down on the right hand side.

#. In the ``Automate Action`` section, select ``Reboot VM...``.

#. This automated action allows the selected Virtual Machine to be rebooted
   using one of the following methods:

   - Soft Reboot: Graceful shutdown and restart of your server's operating
     system.
   - Hard Reboot: Power cycle your server (immediate shutdown and restart).
     You need to select a reason for a ``Hard Reboot`` from the dropdown list.

Filtering virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following steps to filter the view of your virtual machines:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The Virtual Machines
   management section displays.

#. Click to filter the virtual machines by:

   - All Virtual Machines
   - Status: Online or Powered Off
   - Type: Virtual Machine, Clone, or Template
   - Region (Datacenter)
   - Hypervisor

Snapshotting a virtual machine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. warning::

   As snapshot files grow, it can affect all virtual machines on the
   hypervisor. For this reason, Rackspace recommends keeping no longer
   than a two-day snapshot. After this time, you can delete the snapshot,
   or we can revert to the to the snapshot and original disks.

A VMware snapshot is a copy of the virtual machine's disk file (VMDK) at a
given point in time. Snapshots provide a change log for the virtual disk
and are used to restore a VM to a particular point in time when a failure
or system error occurs.

Use the following steps to snapshot a virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section displays.

#. Select the virtual machine you wish to snapshot.

#. Scroll to the ``Snapshots`` section.

#. Click ``Create Snapshot``.

#. Enter a description for your new snapshot.

Reverting snapshots
-------------------

Use the following steps to revert a snapshot of a virtual machine:

.. warning::

   You will lose all changes made to this virtual machine after the snapshot
   was created. You cannot undo this action.

#. Click the gear icon next to the selected ``Snapshot name``.

#. Click ``Revert to Snapshot``.

#. Click ``Revert``.

   .. warning::

      You lose all changes made to this VM since the snapshot was
      created. You cannot undo this action.

#. The virtual machine automatically powers down and powers back on after.

Deleting snapshots
------------------

Use the following steps to delete a snapshot of a virtual machine:

.. warning::

   Deleting a snapshot means that all changes that have occurred
   to the virtual machine will get committed to the parent disk or snapshot.

   You lose the ability to restore to your pre-snapshot virtual machine.

#. Click the gear icon next to the selected ``Snapshot name``.

#. Click ``Delete Snapshot``.

This applies all the changes to the virtual machine since the snapshot
was created. The snapshot file applies to the source disk and
the virtual machine stays online during this process. The snapshot no
longer exists.

.. warning::

   As snapshot files grow, it can affect all virtual machines on the
   hypervisor. For this reason, Rackspace recommends keeping no longer than
   a two-day snapshot. After this time, you can delete the snapshot, or we
   can revert to the to the snapshot and original disks.

Resizing and adjusting virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
.. warning::
   It is important to size VMs as close to what is required as possible as
   resources like CPU, memory, and disk can be easily added but removal requires
   a restart and results in downtime.

Rackspace recommends the following resource allocation ratios:

* 1:5 physical CPU to virtual CPU
* 1:1.5 physical RAM to virtual RAM

Before resizing a virtual machine, note that overallocation of resources has
the potential to negatively impact the performance of the virtual machine and
other virtual machines within your environment.

Use the following steps to resize and adjust a virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section appears.

#. Select the virtual machine that you want to resize from the virtual machine
   list. This action opens up your individual virtual machine's details.

#. Click the ``Actions`` dropdown menu on the right-hand side.

#. In the ``Automate Action`` section, select ``Resize VM...``. This
   automatically shuts down your VM, applies your change, and powers
   the VM back on.

#. Choose the new number of ``vCPUs`` and amount of ``vRAM``.

#. Click ``Resize Virtual Machine``.

   .. warning::

      Clicking ``Resize Virtual Machine`` causes your virtual machine to power
      off immediately. This process takes approximately 5 minutes plus
      the required boot time.


Re-imaging virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following steps to request a re-image a virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section displays.

#. Select the virtual machine that you want to clone from the virtual machine
   list. This action opens up your individual virtual machine's details.

#. Click the ``Actions`` drop-down on the right hand side.

#. In the ``Automate Action`` section, select ``Re-image VM...``.

#. This action request reprovisions this VM with a new Guest OS version
   or a new Guest OS. Provide details of any needing to be
   retained in current VM prior to reprovisioning.

#. Click ``Request Re-Image``.


#. This action creates a ticket to track your re-imaging.

   .. warning::

      You lose all data on your VM once re-imaged. Save any data
      you might need elsewhere. The VM will be unavailable for several
      hours during the re-imaging process.

Removing and deleting virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use the following steps to delete a virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section appears.

#. Select the virtual machine you wish to **remove** from the virtual machine
   list. This action opens up your individual virtual machine's details.

#. Click the ``Actions`` dropdown menu on the right-hand side.

#. In the ``Request Action`` section, select ``Delete VM...``.

#. Enter any ``Special Instructions`` to include in support ticket.

#. Select ``Request Deletion``

This action triggers a ticket for your Rackspace VMware Support team specialist
to action. To track the progress of this, see the Tracking Orders section
below.

Tracking orders
~~~~~~~~~~~~~~~

If you have requested the creation of a new VM, re-imaging, or the deletion of
a VM you can track your order through the MyRack portal.

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section displays.

#. Select ``Track Orders``.

If you have any concerns or questions about an action you have requested,
contact your Rackspace VMware Support team specialist.
