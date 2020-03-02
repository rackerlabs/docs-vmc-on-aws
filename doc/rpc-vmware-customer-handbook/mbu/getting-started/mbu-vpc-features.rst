============
MBU features
============

The Managed Backup (MBU) service provides full image backup of all the
discovered customer VMs.
Upon customer request, MBU can perform full image restoration of one
or more customer VMs.

MBU does not provide file-level or application-level backup and
restores.


Fully managed by Rackspace
~~~~~~~~~~~~~~~~~~~~~~~~~~

Rackspace supports MBU with 24x7x365 coverage.


Snapshot-based backup and restore
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

All VMs are backed up live by using snapshots. This provides a
crash-consistent backup of all data within the VM and the VM
properties. A VM can be restored in its entirety when requested.
File-level restores are not provided, but you can request to restore a
VM image-level backup as a different VM name, which would enable you
to connect the VM disk file to the original VM and copy the necessary
files from it.


Backup service options
~~~~~~~~~~~~~~~~~~~~~~

The service is configured for daily incremental backups and weekly
full backups. You can choose the following retention options:

- Two-week or four-week onsite disk-based backup retention
- Four-week, 12-week, or 52-week offsite tape-based retention



Integrated with the RPC-VMware product
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The service is configured to connect to the vCenter Server with backup
options configured at the vSphere cluster level. This configuration
enables the autodiscovery of new VMs so there is no need to configure
backups for each VM separately. If you want to disable backups for a
specific VM, you can contact Rackspace Support.
