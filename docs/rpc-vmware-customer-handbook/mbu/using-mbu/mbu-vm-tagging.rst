==========
VM tagging
==========

When using Managed Backup (MBU), you can configure the backups
based on ``tagging``.

A tag is a label that you can apply to objects in the vSphere
inventory. When you create a tag, you assign that tag to a category and
categories allow you to group related tags together.

The default RPC-VMware configuration configures backups to backup every VM that
reside in a resource pool or cluster. If you use tags, you can explicitly
define the content you backup which allows you to remove or add VMs from
backup without involving MBU.

With tags you can define what content you backup, giving you more control over
your VMs. By using tags, you can remove or
add VMs from the backup content without involving MBU.

Use cases
~~~~~~~~~

Customers of RPC-V can configure backups based on tagging for the
following scenarios:

#. Customers that only want certain VMs backed up can have that VM
   tagged. Rackspace configures only the backup content to a specific tag.

#. Customers that do not want certain VMs backed up can use a ``Do Not Backup``
   tag to every VM that this applies to. As a result, Rackspace only
   configures backups for VMs that do not have this tag applied.

.. important::

   It is up to the customer or the Rackspace VMware support team to create
   the VM tags in vCenter. You must ensure that MBU is updated with the naming
   conventions of the VM tags so that MBU can configure accordingly.

   MBU does not create the VM tags in vCenter.

Configuring Rackspace Managed Backups based on tagging
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. For RPC-V customers, Rackspace can exclude a set of VMs based on the ``Tag``
   in vCenter. The VM tag needs to be setup first in the vCenter before MBU
   can identify the new options.

   Examples of a VM tag in vCenter:

   .. figure:: ../../../figures/mbu_example1.png
      :alt: MBU Example 1

   .. figure:: ../../../figures/mbu_example2.png
      :alt: MBU Example 2

Configuring backups based on VM Tag in the GUI
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following instructions configure backups to exclude VMs based on
tagging. This is the most common use case for VM tagging and MBU.

#. Click ``Add``. The ``Tags and Categories`` drop-down appears.

   .. figure:: ../../../figures/mbu-tags-categories.png
      :alt: Tags and Categories

#. The filter appears as ``No Backup``. This is because it was tagged in
   vCenter as ``No Backup``.

   .. figure:: ../../../figures/mbu-tags-step-2.png
      :alt: Subclient properties of Tagging

   If you want to define content by tagging, contact your Rackspace VMware
   support team to provide the naming convention for the VM tag. This is so
   Rackspace can define the content with that specific tag.
