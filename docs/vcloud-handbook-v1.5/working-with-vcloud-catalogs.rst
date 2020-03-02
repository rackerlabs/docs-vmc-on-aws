=====================
Working with catalogs
=====================

Rackspace provides Dedicated vCloud customers with a catalog of vApp
templates to use when creating vApps with various operating systems. The
Rackspace Catalog is subscribed to a Content Subscription Endpoint using
the VMware Content Subscription Protocol (VCSP). This catalog is hosted
as a web service in a central location for each Rackspace data center
and synchronized between all Rackspace data centers with array-based
replication. The vCloud Director Cells have access to this using the
back-end services network.

More information about vApp templates, including a full list of the
current vApp templates offered in the Rackspace Catalog can be found at
:ref: `catalog-templates`.

The Rackspace catalog is provided by default to Dedicated vCloud
customers. This section discusses how to add and manage additional
catalogs.

**Creating a customer catalog**

#. Sign in to the organization where the catalog will be created.

#. Select the **Catalogs** tab.

#. Click the green **+** sign to create a new catalog.

#. Enter a name and description for the catalog.

#. If items in the catalog need to be accessed by users other than the
   original creator of the catalog, select the users or groups with
   which the catalog needs to be shared An item can be shared to all
   users in an organization by selecting the **Everyone in the
   Organization** option.

#. If the organization has permission to publish a catalog, the
   **Publishing the Catalog** is available. Publishing a catalog enables
   all organizations in the vCloud Director instance to access it. The
   access is read-only; other organizations can deploy items from the
   catalog but cannot add or remove items from the catalog.

.. note::

   Sharing across organizations is prohibited. If other organizations
   require access to a catalog, it must be published. After a catalog is
   published, all organizations can read it. Please contact Rackspace
   support for catalog publishing assistance.


**Accessing a Catalog**

#. Click **Catalogs**.

#. In the left pane, select one of the following catalog options:

   - **My Organization's Catalogs**

   - **Public Catalogs**

#. In the right pane, select a catalog, right-click, and select
   **Open**.

**Sharing a catalog**

Shared catalogs are available to users in your organization. Users with
the correct rights and access level can use vApp templates and media
from the shared catalog to create their own vApps.

The actions a user can perform on a catalog and its contents depend on
the rights of the user and their access to the catalog. Sharing a
catalog with full control does not grant a user rights that the user
does not already have.

#. Click **Catalogs**.

#. Select **My Organization's Catalogs**.

#. Right-click a catalog and select **Share**.

#. Click **Add Members**.

#. Select the users and groups to share with.

   - **Everyone in the organization** Select this option to share the
      catalog with everyone.

   - **Specific users and groups** Select this option, click specific
      users and groups, and click **Add**.

#. Select an access level and click **OK**.

#. Click **OK**.

**Deleting a Catalog**

When deleting a catalog, it must not contain any vApp templates or media
files. These items can be moved to a different catalog or deleted.

#. Click **Catalogs**.

#. Select **My Organization's Catalogs**.

#. Right-click on a catalog and select **Delete**.

#. Click **Yes** to confirm the deletion.
   The empty catalog is deleted from your organization.
