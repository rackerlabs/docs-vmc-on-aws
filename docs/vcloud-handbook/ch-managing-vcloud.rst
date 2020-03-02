=========================
Managing Dedicated vCloud
=========================

This section describes the vCloud Director interface and the following
tasks:

- Accessing the Dedicated vCloud environment

- Setting user preferences

- Managing virtual data centers

- Resetting vApp leases

vCloud Director tabs
~~~~~~~~~~~~~~~~~~~~

The vCloud Director interface contains the following tabs.

- The **Home** tab displays the running vApps in the environment and
  the number of days until their Lease expires. On the right side of
  the page, a **Tasks** section gives quick access to most tasks and to
  organization management links.

- The **My Cloud** tab displays the vApp and VMs. The tag also displays
  expired items and logs. This tab enables creation of vApps from
  Catalog or OVF.

- The **Catalogs** tab displays the Catalogs, vApp Templates, and
  Media. The resources to create new vApps and the Rackspace-provided
  catalogs of VM templates are also displayed. The Rackspace catalog is
  read-only, but any additional catalogs will be available through the
  following sub-tabs:

   - The **Media & Other** tab is where ISOs can be uploaded or
     accessed.

   - The **vApp Templates** is where new Templates can be loaded.
     Modified or existing Templates can be copied and removed from the
     inventory.

   - The **Catalogs** tab is where catalogs can be accessed and some
     properties can be changed.

Accessing the Dedicated vCloud environment
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The vCloud environment is accessible via web browser. Rackspace provides
the URL for the vCloud Director web console.

.. note::

   vCloud is only accessible over a VPN connection to Rackspace. This can
   be configured for site-to-site VPN and/or single user VPN connections.
   Rackspace provides VPN details.

#. Navigate to the URL in the browser.

   A login screen appears.

#. Enter the login and password details and press Enter.

Setting user preferences
~~~~~~~~~~~~~~~~~~~~~~~~

To set user preferences, click the **Preferences** link at the top right
of the page to open the **Edit User Preferences** menu.

You can set the following preferences:

-  Default login page

-  The length of time to send out Lease Alerts before the time of
   expiration

You can also change a password by selecting **Change Password**.

Managing and monitoring virtual data centers
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To manage a virtual data center, navigate to the **Home** page and click
**Manage VDCs** on the top right of the page. Most of the settings here
are grayed out and cannot be changed. Please contact support if any of
these settings need to be changed.


**Monitoring virtual data centers**

Monitoring the available resources is important. The following procedure
shows where to audit vApps, Templates, Media, Storage Policies, and
available Org VDC Networks.

#. On the **Home** page, click **Org Settings** on the top right of the
   page.

#. Under **Cloud Resources**, click **Virtual Datacenters**. All Virtual
   data centers (VDCs) and their Allocation Model are displayed.

#. Click on the **Monitor** tab to see the current resources used by the
   You can review the following information:

   -  vApps and their running status

   -  Templates, Media, Storage Policies

   -  Org VDC Networks and their current IP Pool consumption

Managing vApp Leases
~~~~~~~~~~~~~~~~~~~~

To reset the lease on a vApp, it is not necessary to wait for it to
expire.  A vApp can be reset before it expires if the vApp is required
for longer than expected. Expired leases can be renewed or deleted.


**Resetting a lease**

#. Click **My Cloud**.

#. In the left pane, click **vApps**.

#. Select a vApp, right-click, and select **Properties**.

#. On the **General** tab, select the **Reset leases** check box, select
   a runtime and storage lease, and click**OK**.


**Resetting an expired lease**

#. Login to the console and click the **My Cloud** tab.

#. On the left-hand menu click the **Expired Items**, **Expired vApps**,
   or **Expired vApp Templates** tab depending on the type of lease to
   reset.

#. Locate the expired vApp for which you want to reset the lease. Right
   click on the vApp and select **Renew**.

   The restored vApp appears on the **vApps** page.


**Deleting an expired lease**

#. Login to the console and click the **My Cloud** tab.

#. On the left-hand menu click the **Expired Items**, **Expired vApps**,
   or **Expired vApp Templates** tab depending on the type of lease to
   delete.

#. Locate the expired vApp for which you want to delete the lease. Right
   click on the vApp and select **Delete**.

   The vApp is deleted from the list.

