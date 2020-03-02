=============
GOSS features
=============

The Guest OS Services (GOSS) uses an indexing service as well as an enrollment
process to enable GOSS for VMs that you specify.

Virtual machine indexing
~~~~~~~~~~~~~~~~~~~~~~~~

Rackspace will configure an indexing service to connect to your vCenter
server. The indexer will create Configuration Management Data Base (CMDB)
entries for each virtual machine that you create in the RPC-VMware
environment. The virtual machines that have been indexed will become visible
to you in the MyRackspace Portal. This enables you to enroll the indexed
VMs in GOSS. Each indexed VM has vCenter attributes added to the VM
container object in vCenter.

.. note::
  Do not change or remove the attributes or you will not be able to enroll the
  VM in GOSS.

If you add GOSS to your RPC-VMware environment after VMs have been created. It
will be necessary to request that CMDB entries for VMs that you wish to enroll
in GOSS be created so that you can use the automated enrollment process.

Service enrollment
~~~~~~~~~~~~~~~~~~

The service enrollment process allows you to provide Rackspace with a list of
the virtual machines that you want to enable GOSS on, indicate the specific
services desired and to provide Rackspace with OS login credentials that will
be used to perform changes, updates and additions to the operating system. The
service enrollment is an automated process. Any failures in the automated
processes might result in manual remediation efforts to complete the
enrollment.

Configuration changes
~~~~~~~~~~~~~~~~~~~~~

The indexer identifies when various configuration changes occur for Virtual
Machines. The following configuration change triggers additional automation
actions.

- VM Power Off/On: This change triggers updates to the CMDB entry for the
  Virtual Machine to ensure that Rackspace support and automation systems are
  aware when the operating system within the Virtual Machine is expected to be
  accessible.

VM deletion
~~~~~~~~~~~

The indexer identifies when you delete a Virtual Machine from your RPC-VMware
environment and automatically remove the corresponding CMDB entry. If the
Virtual
Machine was enrolled in GOSS, the assigned Public IP and firewall NAT are
removed.
