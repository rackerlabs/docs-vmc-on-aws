=============================
Working with virtual machines
=============================

vCloud Director uses vApps as containers for all VMs. A vApp may contain
one or more VMs. To create a VM, a vApp must be created first. Refer to
:ref:`working_with_vapps` for more information.

Currently, the following limitations apply:

- There is no copy function available. Rackspace recommends creating
  new VMs. However, if a copy is required, contact the Rackspace
  support team.

- Migrating your existing VMs to Rackspace requires that they are
  packaged in OVF or OVA formats and imported into vCloud Director as a
  VM or template. Please refer to the documentation of the source
  system for instructions on exporting to these formats. For additional
  information about migrating workloads to Dedicated vCloud, contact
  Rackspace Support.

.. note::
   To make changes to an element that appears grayed out, shut down the VM
   and make the changes while it is powered off.

Managing virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~

**Adding a VM to a vApp**

#. Double-click on the vApp.

#. Click on the green **(+)** button to add a single VM to the vApp.

#. Select the VM(s) to add from the catalog and click on Add, or create
   a completely new VM by clicking on **New Virtual Machine**.

#. If choosing **New Virtual Machine**, pick the machine name and
   hardware settings.

#. Select the storage profile where the new VMs are to be placed.

#. Select the network connectivity.

#. Customize the hardware of the VM before adding it to the vApp.

#. After clicking on Finish in the wizard window, the VM(s) will be
   added to the current vApp.


**Restarting a VM**

#. Right click on a VM and select **Shut Down Guest OS**.

#. Right click on the VM and select **Power On**.


**Suspending and resuming the VM**

#. Right click on a VM and select **Suspend**.

#. Right click a **VM** and select **Resume**.


**Modifying the VM**

#. To modify a vApp or VM, right click it and click **Properties**.

#. Edit the lease, CPU and Memory as needed.


**Deleting the VM**

#. Shut down the VM.

#. Right click and click **Delete**.

#. Delete any ACLs created on personal firewalls in the MyRackspace
   portal.

.. warning::
   When a VM is deleted, it is not retrievable. Rackspace does not maintain
   backups of VMs. Rackspace recommends that users create their own backups
   in case of accidental deletion.

   Organization policies can be used to preserve VMs for a short period of
   time after deletion by setting a vApp Storage Cleanup option. This
   feature is disabled by default since a deleted VM will continue to
   occupy storage resources until the cleanup delay time expires and the VM
   is actually deleted from storage. To request customization of any
   settings in your Dedicated vCloud environment, please contact Rackspace
   support.

VM Console
~~~~~~~~~~

To access the VM console, right click on a VM and click **Popout
Console**. You can also access the VM by double clicking on its icon.

.. note::
   When first connecting to a console, the browser may prompt the download
   of a client plug-in for the console. The certificate of the console may
   need to be manually accepted prior to access a console session. To
   manually accept the certificate point, open the custom console URL in
   your browser.

Snapshots
~~~~~~~~~

A snapshot captures the state of a VM.

- To create a snapshot, right click on a **VM** and click **Create
  Snapshot**.

- To revert back to a previous snapshot click **Revert to Snapshot**.

- To delete an unneeded snapshot click **Remove Snapshot**.

When reverting to a previous snapshot, Rackspace recommends removing the
snapshot as soon as the new VM's settings have been confirmed and the VM
is working as expected. Performance will decrease as time elapses
between the snapshot and any updates. As the delta file continues to
grow, the VM can become unstable or experience data loss. Running out of
disk space can cause not only the snapshot VM to become unresponsive,
but also any other VMs running on the same data store.

Downloading a VM as a template
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To download a VM as a template from Dedicated vCloud, submit a request
to Rackspace to enable a template or media file in the catalog for
download. When the request is met, the item can be downloaded from the
catalog. You can also save an existing Rackspace provided or customer
provided VM as a template in the catalog and request that Rackspace
enable the template for download.

.. note::
   The ability to download an existing powered-off vApp is currently
   disabled.
