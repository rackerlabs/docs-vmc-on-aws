====================
Request a VM restore
====================

#. Log in to the MyRackspace portal.

#. In the navigation pane at the top of the window, click
   :guilabel:`Services > Managed Backup`.

   .. figure:: ../../../figures/mbu-vpc-services-pane-1.png
      :alt: MBU Services pane

#. Locate the VM that you want to restore.

   .. note:: MBU does not allow file-level restores. Only full VMs can
             be restored.

   .. figure:: ../../../figures/mbu-vpc-tasks-vm-1.png
      :alt: MBU VM pane

#. Click :guilabel:`Request Restore`.

#. Under :guilabel:`Restore from Backup`, select the date of the
   backup that you want to restore.

   .. figure:: ../../../figures/mbu-vpc-backup-date-1.png
      :alt: MBU backup date pane

#. Enter information about the VM restore in the following fields:

   :guilabel:`Full Path and Filenames`
     The full path and name of the VM being restored.

   :guilabel:`Where would you like the files restored to?`
     The location where the VM restore should be placed.

   :guilabel:`Special Instructions`
     Any special instructions regarding the VM restore.

#. Click :guilabel:`Request a Restore`.

The restore request is submitted.
