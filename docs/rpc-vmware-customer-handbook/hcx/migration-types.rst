===================
HCX migration types
===================

Cold Migration (offline)
~~~~~~~~~~~~~~~~~~~~~~~~

This migration method uses the VMware NFC protocol. It is automatically
selected
when the source virtual machine is powered off.

vMotion (no downtime)
~~~~~~~~~~~~~~~~~~~~~

A live migration of a single VM at a time with no downtime. This is similar to
a
standard vSphere vMotion, and is most useful when migrating production critical
VMs that have high availability requirements and zero downtime is desired.

vMotion and cold migration transfers a single virtual machine at one time. For
example, if you plan to transfer 100 VMs, HCX will transfer each of these
machines in a serial fashion; one transfer at a time. So while this
method gives you the ability to rapidly migrate a VM, it doesn’t provide you
with a mechanism to migrate VMs in bulk.

HCX Bulk Migration (low downtime)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This migration method uses the VMware vSphere Replication protocols to move the
virtual machines to a remote site.

The Bulk migration option is designed for moving virtual machines in
parallel.

This migration type can set to complete on a pre-defined schedule.

The virtual machine runs at the source site until the failover begins. The
service interruption with bulk migration is equivalent to a reboot.



Cloud Motion with vSphere Replication (no downtime)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This is a relatively newer migration method currently available in preview for
VMware Cloud on AWS. It combines the benefits of bulk migration (parallelism,
scheduling, etc.) with the ability to migrate live workloads with no downtime.

-	Uni-directional from on-premises to VMware Cloud on AWS
- Supports source vSphere (vCenter Server / ESXi) versions 5.5 and above
- Cross-version migration from vSphere 5.5 to the current release of 6.7
  Update 1
- Currently no support for on-premises to on-premises migrations
- Concurrent migrations = 100 (initial data sync using vSphere Replication)

HCX Reverse Migration
~~~~~~~~~~~~~~~~~~~~~

This feature provides you the ability to migrate VMs from your cloud
environment
to your on-premises environment using vMotion, Cold, and Bulk migration
methods.
This is useful for situations in which it’s determined that a transferred VM–or
set of VMs–isn’t suitable for the cloud.
