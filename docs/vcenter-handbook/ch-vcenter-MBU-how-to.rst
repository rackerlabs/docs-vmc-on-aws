====================
Using Managed Backup
====================

This section describes the following Managed Backup (MBU) tasks:

-  Reviewing VM Backups in vCenter

-  Requesting a VM Restore

-  Excluding a VM from Backup

Reviewing VM Backups in vCenter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Log in the vCenter webclient.

2. Locate the VM you are checking.

3. Click the **Monitor** tab.

4. Click the **Tasks** tab.

   .. image:: ../figures/MBU_MyRackspace-Tasks-tab.png

5. Select the most recent task named **Set virtual machine custom value**.

   The backup information is located under **Related events:** at the bottom of
   the **Tasks** tab. The backup entry reads *Changed Custom Field Last Backup
   on <VM NAME> in <Datacenter in vCenter> to <date/time>*.

Requesting a VM Restore
~~~~~~~~~~~~~~~~~~~~~~~

1. Log in to MyRackspace.

2. Select the **Services** tab in the navigation pane, and click **Managed
   Backup**.

   .. figure:: ../figures/MBU_MyRackspace.png

3. Locate the VM you want to restore.

   .. figure:: ../figures/MBU_devices.png

4. Click **Request Restore** under the VM being restored.

5. Select the date of the backup you want to restore from under **Restore from
   Backup**.

   .. figure:: ../figures/MBU_backups.png

6. Enter information about the VM restore in the following fields:

   * *Full Path and Filenames*: The full path and name of the VM being
     restored.

   .. note::
      MBU does not allow file level restores. Only full VMs can be restored.

   * *Where would you like the files restored to?*: The location where VM
     restore should be placed.

   * *Special Instruction*: Any special instructions regarding the VM restore.

   .. figure:: ../figures/MBU_path-information.png

7. Click the **Request a Restore** button.

   The restore request is submitted.

Excluding a VM from Backup
~~~~~~~~~~~~~~~~~~~~~~~~~~

Backups are configured to discover VMs automatically. If there is a VM that you
do not not want to be backed up, you will need to submit a ticket through
MyRackspace. You will need to supply the following information in your ticket:

   * Cluster name

   * Host name

   * Name of VM to exclude

.. note::

   A complete inventory of all VMs being backed up can be accessed through
   vCenter.
