:orphan:

============================================================================
Installing End Point Operations Management Agents and Verify Data Collection
============================================================================

VMware® vRealize® Operations™ (vROps) is used to monitor all virtual machines
(VMs) in your cluster. However, vROps with End Point Operations (EP Ops)
agents must be installed to get customer-managed guest OS and application
(Microsoft® SQL Server™, Microsoft Active Directory®, Apache® Tomcat™, and
PostgreSQL®) monitoring.

This document includes the following procedures to assist in using vROps:
   * Locating EP Ops agents files
   * Installing EP Ops agents
   * Uninstalling EP Ops agents
   * Verifying that EP Ops agent is collecting data
   * Viewing EP Ops specific metrics
   * Viewing EP Ops specific alerts

.. _locating_ep_ops_agents:

Locating EP Ops agents files
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The EP Ops agent files are located in the ``vROps End Point Agents`` folder
in the local VMFS datastore on the first ESXi host in your inventory. These
consist of zip files for Microsoft Windows® and tar files for Linux and are
available in both x32 and x64 formats.

#. From the vSphere Client or vSphere Web Client, select the first ESXi host
   in the inventory.

#. Browse to its local datastore and download the files to the desktop or to
   a central location.

#. Copy the downloaded files to VMs that need to be monitored. Use the
   procedures below to install the monitoring agents.

.. note::
   The EP Ops agents installation files that include Java will overwrite
   your current Java version. To configure the EP Ops agent to use a
   different version of Java than the one installed on the Virtual Machine,
   refer to the `vRealize Operation Manager Installation and Configuration Guide
   <http://pubs.vmware.com/vrealizeoperationsmanager-61/topic/com.vmware.ICbase/PDF/vrealize-operations-manager-61-linux-windows-install-guide.pdf>`_
   for instructions.

Installing EP Ops agents
~~~~~~~~~~~~~~~~~~~~~~~~

An EP Ops agent must be installed on every VM you want to monitor. Use the
following procedures to install the downloaded files on a Linux or Windows
VM.

**Installing EP Ops agent on Linux**

#. Locate the Linux (tar) EP Ops agent installation files (x32-bit or
   x64-bit) as described in :ref:`locating_ep_ops_agents`.

#. Copy the installation file to the VM where you want to install the
   agent:

   .. code-block:: console

      $ tar -zxvf epops-agent-x86-64-linux-xxx.tar.gz

#. Change directory to the EP Ops agent bin directory:

   .. code-block:: console

      $ cd /epops-agent/bin

#. Run ``ep-agent.sh`` with ``start`` parameter and enter the correct
   information when prompted:

   .. code-block:: console

      $ ./ep-agent.sh start

   .. code-block:: console

      Enter the server hostname or IP address: Enter IP of the vROps Server
      Enter the server SSL port [default=443]: Press Enter to accept the default
      Are you sure you want to trust this certificate (yes/no/more)? Yes
      Enter your server username: vCenter Login
      Enter your server password: vCenter Password

**Installing EP Ops agent on Windows**

#. Locate the Windows (zip) EP Ops agent installation files (x32-bit or
   x64-bit) as described in :ref:`locating_ep_ops_agents`.

#. Copy the installation file to the VM where you want to install the
   agent.

#. Extract the EP Ops agent zip file located on the VM to the
   ``C:\epops-agent`` directory locally.

#. Open the command prompt and change directory to the EP Ops agent bin
   directory:

   .. code-block:: console

      C:\ cd C:\epops-agent\bin

#. Install the EP Ops agent service:

   .. code-block:: console

      C:\epops-agent\bin> ep-agent.bat install

#. Run ``ep-agent.bat`` with ``start`` parameter and enter the correct
   information when prompted:

   .. code-block:: console

      C:\epops-agent\bin> ep-agent.bat start

   .. code-block:: console

      Enter the server hostname or IP address: Enter IP of the vROps Server
      Enter the server SSL port [default=443]: Press Enter to accept the default
      Are you sure you want to trust this certificate (yes/no/more)? Yes
      Enter your server username: vCenter Login
      Enter your server password: vCenter Password

Uninstalling EP Ops agents
~~~~~~~~~~~~~~~~~~~~~~~~~~

If you no longer want to monitor a guest OS on a particular VM, you must
uninstall the EP Ops agent from the VM. If you want to reinstall the
agent on a particular VM, first uninstall the agent. Simply deleting the
directory will not allow a new installation of the EP Ops agent to
successfully install.

**Uninstalling EP Ops agent on Linux**

#. Change directory to the EP Ops agent bin directory:

   .. code-block:: console

      $ cd /epops-agent/bin

#. Stop the EP Ops agent:

   .. code-block:: console

      $ ./ep-agent.sh stop

#. Delete the data directory:

   .. code-block:: console

      $ rm -rf /opt/epops-agent/data

#. Delete the ``epops-token`` file:

   .. code-block:: console

      $ rm /etc/vmware/epops-token

**Uninstalling EP Ops agent on Windows**

#. Open the command prompt and change directory to the EP Ops agent bin
   directory:

   .. code-block:: console

      C:\ cd C:\epops-agent\bin

#. Stop the EP Ops agent:

   .. code-block:: console

      C:\epops-agent\bin> ep-agent.bat stop

#. Remove the EP Ops agent service:

   .. code-block:: console

      C:\epops-agent\bin> ep-agent.bat remove

#. Delete the data directory using the command line or Windows Explorer:

   .. code-block:: console

      C:\epops-agent> rd /s data

   .. code-block:: console

      Are you sure (Y/N)? Y

#. Delete the ``epops-token`` file using the command line or Windows
   Explorer:

   .. code-block:: console

      C:\epops-agent> del "C:\ProgramData\VMware\EP Ops agent\epops-token"

   ..  note::

       If using Windows Explorer, enable **Show hidden files, folder, and
       drives** in the **Folder Options**.

Viewing EP Ops agent data
~~~~~~~~~~~~~~~~~~~~~~~~~

This section describes how to verify that the EP Ops agent is collecting
data, and how to view EP Ops specific metrics and alarms.

**Verifying that the EP Ops agent is collecting data**

#. Log in to vROps and click **Administration**.

#. Click **Inventory Explorer** in the left navigation pane.

#. Click **Adapter Instances** in the **Inventory Explorer** window.

#. Click **EP Ops Adapter Instance**, located under **Adapter Instances**.

#. Click **EP Ops Adapter**, located under **EP Ops Adapter Instance**.

   Reporting VMs are listed as **EP Ops agent – *{VM Name}***.

#. Select an EP Ops adapter to see the status of the agents.

   The image below displays two VMs listed as **Lab-Win12** and
   **LabUbuntu**.

   .. figure:: ../figures/Listed_VMs.png

   Verify that all listed agents are receiving (green) for both
   **Collection State** and **Collection Status**.

   .. figure:: ../figures/collecting_data.png

**Viewing EP Ops metrics**

vROps with End Point Operations Management adds operating system (OS) metrics
and metrics for a few popular applications to get a granular view of what is
happening inside your VM.

#. Log in to vROps and click **Environment**.

#. Click **Operating Systems** in the left navigation pane.

#. Expand the folders under **Operating Systems World** to see the
   different **Operating System** categories. Expand those categories to
   see the VMs with agents installed.

#. Click on a VM, and then click on the **Troubleshooting** tab in the
   right pane.

#. Click the **All Metrics** tab under **Troubleshooting** to list the
   EP Ops specific metrics.

#. Double click a metric to see a line graph representation of the data.

   .. figure:: ../figures/vRealize_metrics.png

**Viewing EP Ops specific alerts**

vROps with End Point Operations Management adds alerts specific to
operating systems to get a broader view of what is happening inside your
VM.

#. Log in to vROps and click **Content**.

#. Click **Alert Definitions** in the left navigation pane.

#. Filter the list by clicking **All Filters** and choosing **Adapter Type**.

#. Enter ``EP Ops`` in the pop-up box and click **OK** to see all the
   active alerts related to EP Ops.

   .. image:: ../figures/vRealize_alerts.png
      :alt: vRealize alerts
