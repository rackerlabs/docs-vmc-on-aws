.. _working_with_vapps:

==================
Working with vApps
==================

vCloud Director uses vApps as containers for all VMs. A vApp may contain
one or more VMs. Before creating a VM, a vApp must be created first. By
default all vApps and the VMs that they contain can only be seen and
managed by the user that created them. To enable other Dedicated vCloud
users to interact with a vApp it must be shared with them.

**Build a new empty vApp**

#. On the **Home** page, click **Build New vApp**.

#. Enter a name and description for the vApp. Click **Next**.

#. To proceed without creating a VM, Click **Next** on the **Configure
   Resources** page, the **Configure Virtual Machines** page, and the
   **Configure Networking** page.

#. Review the settings and click **Finish** to create the vApp.

   An empty vApp is created. When the process is complete, the vApp can
   be populated with VMs.

**Build a new vApp and add a VM**

#. On the **Home** page, click **Build New vApp**.

#. Enter a name and description for the vApp. Click **Next**.

#. Click **New Virtual Machine** to create a new VM.

#. In the **Configure Resources** page, name the newly created VM.

#. In the **Configure Virtual Machines** page, change the computer name
   as needed.

#. On the **Configure Networking** page, click **Next**.

#. Review the settings and click **Finish** to create the vApp.

   A vApp is created with a VM. When the process is complete, the vApp
   can be populated with more VMs.

**Build a new vApp from OVF**

An OVF file can have one or more VMs inside of it.

#. On the **Home** page, click **Add vApp from OVF**.

#. Browse to the location of the vApp OVF on a local drive or via a URL.
   Click **Next**.

#. Review details and click **Next.**

#. In the **Select Name and Location** page, name the VM and choose the
   VDC.

#. On **Configure Resources** choose the storage policy

#. On the **Configure Networking** page, name the Computer.

#. Choose your Customized Hardware settings of CPU, Memory and Hard Disk
   size.

#. Review the settings and click **Finish** to create the vApp.

   A vApp is created from the OVF file. When the process is complete,
   the vApp can be populated with VMs.

**Restarting a vApp**

#. Right click on a vApp and click **Power Off**.

#. Right click on the vApp and click **Start**.

**Suspending and resuming a vApp**

#. Right click on a vApp and click **Suspend**.

#. Right click the vApp and click **Start**.
