==========
VM actions
==========

After your RPC-VMware environment is configured for Guest OS Services, an
automated system that has been registered with the vCenter Server will receive
vCenter event notifications when certain VM actions are performed by you.

VM event types
~~~~~~~~~~~~~~

This section describes the VM event types.

VM creation
-----------

Virtual Machine (VM) creation notifications are used to determine when new VMs
are
created in RPC-V in order to make them available for GOSS enrollment. When
a create notification is received, the automation system interrogates vCenter
for VM container details that allows a CMDB entry for the VM to be created.
Also, the automation system adds a custom attribute to the VM contain that
contains the CMDB device number associated with that VM.

VM creation events might be triggered by creating a new VM container,
deploying a new VM from a template, deploying a new VM from OVA/OVF, adding a
VM to inventory from the local datastore, migrating a VM into RPC-VMware,
restoring a VM from a backup or certain 3rd party tool functions that result
in the enrolled VM being added to the RPC-VMware vCenter inventory.

.. note::
   It is important that you never remove or modify the custom attribute of the
   VMs in RPC-VMware.

VM power on or off
------------------

When you power off or suspend a VM, automation updates the system status in
the CMDB to
indicate that the VM is offline. When you power on or resume a VM, the system
status
returns to active.

VM deletion
-----------

When you delete, migrate, or unregister VMs in vCenter, the indexing service
automatically removes the CMDB entry for those VMs. You will no longer see
CMDB entries for deleted VMs in the MyRackspace portal. The Public IP assigned
to enrolled VMs that are deleted will now be available for new enrollments.

.. note::
   Unregistering a VM from vCenter is treated the same as deleting a VM. If you
   unregister an enrolled VM and then register it again, the VM is assigned a
   new CMDB number and is not considered enrolled in Guest OS Services.
   Contact your support team prior to taking this action so that they can
   assist with reconfiguring the installed services for the new CMDB number.

VM clone
--------

Cloning a VM triggers a VM creation event as described above. When a VM
enrolled in GOSS is cloned, the internal OS changes that were made during
enrollment are no longer correctly associated with the new CMDB entry. The
cloned VM still contains internal OS associations with the source VM CMDB
entry. When you clone a VM enrolled in GOSS, it is necessary for you to
contact your support team to have the CMDB association corrected in the new
VM.

.. note::
  You might need to reboot the new VM after corrective actions have been
  taken.

VM IP changes
-------------

Changing the local IP of a VM that has been enrolled in GOSS will disrupt the
configured services and associated automated processes as well as the ability
of Rackspace Support to quickly access the OS of your enrolled VMs.

If you need to change the local IP of an enrolled VM, contact your
Support team to coordinate activities necessary to update the Rackspace CMDB
entries and associated hosted firewall NATs.
