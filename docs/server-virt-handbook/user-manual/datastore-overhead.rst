==================
Datastore overhead
==================

Rackspace requires that customers have a certain percentage of
each Virtual Machine File System (VMFS) datastore free at all
times. We call this ``datastore overhead``. The percentage
depends on the total capacity of each datastore. The following are
the minimum recommended values:

- For datastores with capacity up to 2048 GB, the overhead is 15%.
- For datastores with capacity between 2049 GB and 4096 GB, the overhead is
  10%.
- For datastores with capacity greater than 4096 GB, the overhead is 7%.
- If VMs on the datastore are utilizing
  :ref:`VM Replication <svh-vm-replication>`
  or :ref:`VM Recovery <svh-vm-recovery>`, the overhead is 15%. This overrides
  any sizing criteria from the above points.

Why does Rackspace require this?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- If a datastore runs out of free space, it causes any VMs running on that
  datastore to immediately hard stop, causing downtime. Stopped VMs cannot be
  started until insufficient free space on the datastore us available.
- Once VMs are stopped, it is possible that a VM may not power on due to
  insufficient space on the datastore.
- VM performance impact is possible when the datastore is critically low on
  space.
- Certain VMware features, such as snapshots, may no longer function.

What else can consume space on my datastores?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- **Snapshots:**
  When performing a snapshot, a delta disk is created for each vDisk you have
  on
  your VM. While the snapshot is active or a clone is in progress, all changes
  are written to the delta file(s). Delta files can grow rapidly and without
  your awareness.
- **VM log files:**
  All VM log files are stored within the VM container folder
  on the datastore. Normal log files are only a few MB in size. However, log
  files can grow to 5GB in size depending on VM activity and DRS migrations.
- **RAM:**
  Powered on VMs have a vSwap file equivalent in size to the amount of vRAM
  assigned to the VM. For example, a VM with 128 GB of RAM has a 128 GB vSwap
  file. vSwap files only exist for VMs that are powered on. Powering on a VM or
  increasing the amount of vRAM in your VM consumes additional space on the
  datastore.
