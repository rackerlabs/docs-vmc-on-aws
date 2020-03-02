====================================
Components, features and permissions
====================================

This section describes the components of Dedicated VMware vCloud, its
features, and the permissions available to each role.

Dedicated VMware vCloud components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Dedicated VMware vCloud product comprises several VMware services
and a backup system to ensure the availability of those services. The
VMware services operate on a management cluster with two hypervisors,
which increases availability.

The following services are installed in a Dedicated VMware vCloud
environment.

-  vCenter Server

-  vCloud Director Cell - Qty: 2

-  Dedicated Virtual Machine Recovery Appliance

-  vShield Manager

-  Edge FW Appliance - Qty: 2

-  vRealize Operations (vROps) Virtual Appliance

-  VMware Update Manager

.. note::

   Access to these VMware services is limited to the user interface or API
   for vCloud, vCenter, and vROps. Rackspace manages and maintains servers
   running the Dedicated VMware vCloud VMware services.

Dedicated VMware vCloud customer features
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following table provides a list and description of vCloud features
and responsibilities related to vApps, VMs and catalogs.


**vCloud feature responsibility**

+--------------------------+-----------------------+--------------------------+
| Feature                  | Responsibility        | Description              |
+==========================+=======================+==========================+
| Creating one or more     | Customer              | A customer can create    |
| managed VMs as a vApp    |                       | vApps with               |
|                          |                       | Rackspace-managed VMs    |
|                          |                       | using templates provided |
|                          |                       | by Rackspace.            |
+--------------------------+-----------------------+--------------------------+
| Creating one or more     | Customer              | vApps with unmanaged VMs |
| unmanaged VMs as a vApp  |                       | are created using        |
|                          |                       | templates provided by    |
|                          |                       | Rackspace.               |
+--------------------------+-----------------------+--------------------------+
| Creating one or more     | Customer              | vApps with               |
| customer-provided VMs as |                       | customer-provided VMs    |
| a vApp from a template   |                       | using templates created  |
|                          |                       | by uploading OVA/OVF     |
|                          |                       | files to a customer      |
|                          |                       | catalog.                 |
+--------------------------+-----------------------+--------------------------+
| Creating one or more     | Customer              | vApps with blank VMs     |
| customer-provided VMs as |                       | that have an OS          |
| a vApp from an ISO       |                       | installed by connecting  |
|                          |                       | an ISO file from a       |
|                          |                       | customer catalog.        |
+--------------------------+-----------------------+--------------------------+
| Power on/off and         | Customer              | Stop, start and suspend  |
| suspend/resume a VM or   |                       | a VM or vApp.            |
| entire vApp              |                       |                          |
+--------------------------+-----------------------+--------------------------+
| Modify a VM              | Customer              | Changing the resources   |
|                          |                       | of a VM, such as the     |
|                          |                       | CPU, memory, disk, or    |
|                          |                       | name.                    |
+--------------------------+-----------------------+--------------------------+
| Deleting a VM            | Customer              | Deleting a VM.           |
+--------------------------+-----------------------+--------------------------+
| Access to vCloud API     | Customer              | The RESTful vCloud API   |
|                          |                       | used to enable           |
|                          |                       | automation and           |
|                          |                       | integration of           |
|                          |                       | third-party tools (such  |
|                          |                       | as VMware vRealize       |
|                          |                       | Automation) into         |
|                          |                       | Dedicated VMware vCloud. |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | vApps created by         |
| customer-provided OVA as |                       | uploading a OVA/OVF      |
| a vApp                   |                       | template into Dedicated  |
|                          |                       | VMware vCloud.           |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | vApp templates created   |
| customer-provided OVA as |                       | by uploading a OVA/OVF   |
| a template in a customer |                       | template into a customer |
| catalog                  |                       | catalog.                 |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | ISO files stored in      |
| customer-provided ISO in |                       | Dedicated VMware vCloud  |
| a customer catalog       |                       | by uploading it into a   |
|                          |                       | customer catalog media   |
|                          |                       | store.                   |
+--------------------------+-----------------------+--------------------------+
| Read-only access to the  | Customer              | Viewing vCenter          |
| vCenter Server via the   |                       | information with         |
| vSphere API              |                       | read-only permissions    |
|                          |                       | from the vSphere web or  |
|                          |                       | full client, or          |
|                          |                       | third-party software.    |
+--------------------------+-----------------------+--------------------------+
| Accessing the vCloud     | Customer              | Using the Dedicated      |
| Director user interface  |                       | VMware vCloud user       |
|                          |                       | interface to operate     |
|                          |                       | vCloud.                  |
+--------------------------+-----------------------+--------------------------+
| Editing a template or    | Customer              | Modifying the details of |
| media item in a Customer |                       | a template or media item |
| Catalog                  |                       | in a customer catalog.   |
+--------------------------+-----------------------+--------------------------+
| Creating or deleting a   | Customer              | A catalog can be created |
| Customer Catalog         |                       | or deleted on the        |
|                          |                       | provisioned storage to   |
|                          |                       | contain uploaded         |
|                          |                       | templates or ISO files.  |
+--------------------------+-----------------------+--------------------------+
| Changing the Customer    | Customer              | Reassigning the          |
| Catalog Owner            |                       | ownership of a catalog   |
|                          |                       | to a different vCloud    |
|                          |                       | user account.            |
+--------------------------+-----------------------+--------------------------+
| Editing a Customer       | Customer              | Editing the properties   |
| Catalog Properties       |                       | of a created catalog.    |
+--------------------------+-----------------------+--------------------------+
| Publishing a Customer    | Customer              | Choosing which vCloud    |
| Catalog to another       |                       | organizations can access |
| Organization in the same |                       | the created catalog.     |
| vCloud                   |                       |                          |
+--------------------------+-----------------------+--------------------------+
| Sharing a Customer       | Customer              | Selecting users in the   |
| Catalog with other users |                       | vCloud organization to   |
| within the same vCloud   |                       | use the catalog.         |
| Organization             |                       |                          |
+--------------------------+-----------------------+--------------------------+
| Creating, modifying and  | Customer              | Create, modify and       |
| deleting Org vCD         |                       | delete independent       |
| independent disks        |                       | disks.                   |
+--------------------------+-----------------------+--------------------------+
| Sharing a vApp with      | Customer              | Sharing access to a vApp |
| other users in the       |                       | with another user in     |
| vCloud Organization      |                       | their vCloud             |
|                          |                       | Organization.            |
+--------------------------+-----------------------+--------------------------+
| Snapshot a VM or vApp    | Customer              | Creating or reverting to |
|                          |                       | snapshots of VMs or      |
|                          |                       | entire vApps.            |
+--------------------------+-----------------------+--------------------------+
| Removing a snapshot from | Customer              | Deleting snapshots of    |
| a VM or vApp             |                       | VMs or entire vApps.     |
+--------------------------+-----------------------+--------------------------+
| Accessing the VM Console | Customer              | Using the VM console to  |
|                          |                       | interact with a VM.      |
+--------------------------+-----------------------+--------------------------+
| Ticket notification of   | Rackspace             | Notifying a customer     |
| completed VM             |                       | that a VM is ready for   |
|                          |                       | use with a ticket that   |
|                          |                       | includes access          |
|                          |                       | information.             |
+--------------------------+-----------------------+--------------------------+
| Publishing a customer    | Rackspace             | Publishing a customer    |
| catalog for external     |                       | catalog for use between  |
| (VCSP) subscription      |                       | two Dedicated VMware     |
|                          |                       | vCloud environments.     |
+--------------------------+-----------------------+--------------------------+
| Creating a customer      | Rackspace             | Creating a customer      |
| catalog that is          |                       | catalog that is          |
| subscribed to an         |                       | subscribed to an         |
| external (VCSP) catalog  |                       | external vCloud catalog. |
+--------------------------+-----------------------+--------------------------+
| Enabling a customer      | Rackspace             | Enabling                 |
| provided catalog item    |                       | customer-provided        |
| for download             |                       | templates in a catalog   |
|                          |                       | to be downloaded by the  |
|                          |                       | customer.                |
+--------------------------+-----------------------+--------------------------+
| Enabling an unsupported  | Rackspace             | Enabling                 |
| VM catalog item for      |                       | Rackspace-provided       |
| download                 |                       | unmanaged VM templates   |
|                          |                       | in a catalog to be       |
|                          |                       | downloaded by the        |
|                          |                       | customer.                |
+--------------------------+-----------------------+--------------------------+
| Managing vCloud users    | Rackspace             | Managing the vCloud      |
|                          |                       | users and groups for a   |
|                          |                       | customer.                |
+--------------------------+-----------------------+--------------------------+
| Managing vCloud external | Rackspace             | Creating, modifying or   |
| networks                 |                       | deleting external        |
|                          |                       | networks for a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| email settings           |                       | organization email       |
|                          |                       | settings as requested by |
|                          |                       | a customer.              |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| LDAP settings            |                       | organization LDAP        |
|                          |                       | settings as requested by |
|                          |                       | a customer.              |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| policies settings        |                       | organization policies    |
| -leases                  |                       | settings - leases as     |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| policies settings        |                       | organization policies    |
| -quotas                  |                       | settings - quotas as     |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| policies settings        |                       | organization policies    |
| -limits                  |                       | settings - limits as     |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| guest personalization    |                       | organization guest       |
| settings                 |                       | personalization settings |
|                          |                       | (Active Directory        |
|                          |                       | defaults) as requested   |
|                          |                       | by a customer.           |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| federation settings      |                       | organization federation  |
|                          |                       | settings (SAML) as       |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Manual migration of      | Rackspace             | Migrating                |
| Rackspace-managed VMs    |                       | Rackspace-managed        |
| from Server              |                       | customer VMs from the    |
| Virtualization powered   |                       | Server Virtualization    |
| by VMware to Dedicated   |                       | offering to Dedicated    |
| VMware vCloud            |                       | VMware vCloud. This is a |
|                          |                       | manual process that      |
|                          |                       | requires down time for   |
|                          |                       | the VM.                  |
+--------------------------+-----------------------+--------------------------+
| Manual migration of      | Rackspace             | Migrating unmanaged VMs  |
| unmanaged VMs from       |                       | from the Dedicated       |
| Dedicated VMware         |                       | vCenter product to       |
| vCenter Server(TM) to    |                       | Dedicate vCloud. After   |
| Dedicated vCloud         |                       | the migration, the VMs   |
|                          |                       | remain unmanaged by      |
|                          |                       | Rackspace. This is a     |
|                          |                       | manual process that      |
|                          |                       | requires down time for   |
|                          |                       | the VM.                  |
+--------------------------+-----------------------+--------------------------+
| Manual migration of      | Rackspace             | Migration of unmanaged   |
| unmanaged VMs from       |                       | VMs from the Server      |
| Server Virtualization to |                       | Virtualization product   |
| Dedicated VMware vCloud  |                       | to Dedicate vCloud.      |
|                          |                       | After the migration, the |
|                          |                       | VMs remain unmanaged by  |
|                          |                       | Rackspace. This is a     |
|                          |                       | manual process that      |
|                          |                       | requires down time for   |
|                          |                       | the VM.                  |
+--------------------------+-----------------------+--------------------------+
| Manual clone process for | Rackspace             | A copy or template of a  |
| customer-provided VMs    |                       | customer-provided VM.    |
+--------------------------+-----------------------+--------------------------+
| Manual clone process for | Rackspace             | A copy or template of an |
| unmanaged VMs            |                       | unmanaged VM.            |
+--------------------------+-----------------------+--------------------------+


Dedicated VMware vCloud permissions list
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This table lists the permissions and privileges available to different
user roles in vCloud. As a Dedicated VMware vCloud customer, you are
granted the permissions listed as "Customer" in the Responsibility
column. The default vCloud roles are listed as a reference.


**vCloud permissions**

.. list-table::
   :widths: 12 12 12 12 12 12 12 12
   :header-rows: 1

   * - Object
     - Privileges
     - Customer role
     - Org Admin\*
     - Catalog author\*
     - vApp author\*
     - vApp user\*
     - Console only\*
   * - Catalog
     - Add vApp from My Cloud
     -
     - x
     - x
     -
     -
     -
   * - Catalog
     - Change owner
     - x
     - x
     -
     -
     -
     -
   * - Catalog
     - VCSP publish subscribe
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Enable a vApp template or media item for download
     - x
     - x
     -
     -
     -
     -
   * - Catalog
     - Create or delete a catalog
     - x
     - x
     - x
     - x
     -
     -
   * - Catalog
     - Edit properties
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Publish
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Sharing
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - View private and shared catalogs
     - x
     - x
     - x
     - x
     -
     -
   * - Catalog
     - View published catalogs
     - x
     - x
     -
     -
     -
     -
   * - Catalog item
     - Create or upload
     - x
     - x
     - x
     -
     -
     -
   * - Catalog item
     - Edit
     - x
     - x
     - x
     -
     -
     -
   * - Catalog item
     - View
     - x
     - x
     - x
     - x
     - x
     -
   * - Catalog item
     - Checkout (add to My Cloud)
     - x
     - x
     - x
     - x
     - x
     -
   * - Catalog item
     - Copy
     - x
     -
     -
     -
     -
     -
   * - Catalog item
     - Enable download
     -
     -
     -
     -
     -
     -
   * - Disk
     - Change owner
     - x
     - x
     - x
     -
     -
     -
   * - Disk
     - Create
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - Delete
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - Edit properties
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - View properties
     - x
     - x
     - x
     - x
     -
     -
   * - General
     - Administrator control
     - x
     -
     -
     -
     -
     -
   * - General
     - Administrator view
     - x
     - x
     -
     -
     -
     -
   * - General
     - Send notification
     - x
     -
     -
     -
     -
     -
   * - Group or user
     - View
     - x
     - x
     -
     -
     -
     -
   * - Organization
     - Edit federation settings
     - x
     -
     -
     -
     -
     -
   * - Organization
     - Edit leases policy
     - x
     -
     -
     -
     -
     -
   * - Organization
     - Edit password policy
     - x
     -
     -
     -
     -
     -
   * - Organization
     - Edit properties
     - x
     -
     -
     -
     -
     -
   * - Organization
     - Edit quotas policy
     - x
     -
     -
     -
     -
     -
   * - Organization
     - Edit SMTP settings
     - x
     -
     -
     -
     -
     -
   * - Organization
     - View
     - x
     - x
     -
     -
     -
     -
   * - Organization network
     - Edit properties
     - x
     -
     -
     -
     -
     -
   * - Organization network
     - View
     - x
     - x
     -
     -
     -
     -
   * - Organization VDC
     - View
     - x
     - x
     -
     -
     -
     -
   * - Organization VDC gateway
     - Configure services
     - x
     -
     -
     -
     -
     -
   * - Organization VDC network
     - Edit properties
     - x
     -
     -
     -
     -
     -
   * - Organization VDC network
     - View properties
     - x
     - x
     -
     -
     -
     -
   * - Organization VDC storage policy
     - Set default
     - x
     -
     -
     -
     -
     -
   * - vApp
     - Upload
     - x
     - x
     -
     -
     -
     -
   * - vApp
     - Download
     - x
     -
     -
     -
     -
     -
   * - vApp
     - Change owner
     - x
     - x
     -
     -
     -
     -
   * - vApp
     - Copy
     - x
     - x
     - x
     - x
     -
     -
   * - vApp
     - Create or reconfigure
     - x
     - x
     - x
     - x
     -
     -
   * - vApp
     - Delete
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Edit properties
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Edit VM CPU
     - x
     - x
     - x
     - x
     -
     -
   * - vApp
     - Edit VM hard disk
     - x
     - x
     - x
     - x
     -
     -
   * - vApp
     - Edit VM memory
     - x
     - x
     - x
     - x
     -
     -
   * - vApp
     - Edit VM network
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Edit VM properties
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Manage VM password settings
     - x
     - x
     - x
     - x
     - x
     - x
   * - vApp
     - Power operations
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Sharing
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Snapshot operations
     - x
     - x
     - x
     - x
     - x
     -
   * - vApp
     - Use console
     - x
     - x
     - x
     - x
     - x
     - x
