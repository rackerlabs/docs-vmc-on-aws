============================
Review VM backups in vCenter
============================

#. Log in to the vCenter web client.

#. Locate the VM that you want to check.

#. Click the :guilabel:`Monitor` tab.

#. Click the :guilabel:`Tasks` tab.

   .. figure:: ../../../figures/mbu-vpc-tasks-pane-1.png
      :alt: Managed Backup tasks pane

#. Select the most recent task that is named :guilabel:`Set virtual
   machine custom value`.

The backup information is located under :guilabel:`Related events` at
the bottom of the :guilabel:`Tasks` tab. The backup entry reads
:guilabel:`Changed Custom Field Last Backup on <vm name> in <data
center in vCenter> to <date/time>`.
