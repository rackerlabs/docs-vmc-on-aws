====================================
Components, features and permissions
====================================

This section describes the components of Dedicated vCloud, its features,
and the permissions available to each role.

Dedicated vCloud components
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Dedicated vCloud product comprises several VMware services and a
backup system to ensure the availability of those services. The VMware
services operate on a management cluster with two hypervisors, which
increases availability.

The following services are installed in a Dedicated vCloud environment.

- vCenter Server

- vCloud Director

- Dedicated Virtual Machine Recovery Appliance

- vShield Manager

- vRealize Operations (vROps)

- VMware Update Manager

.. note::

   Access to these VMware services is limited to the user interface or API
   for vCloud Director, vCenter Server, and vRealize Operations. Rackspace
   manages and maintains servers running the Dedicated vCloud services.

Dedicated vCloud customer features
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The following table provides a list and description of Dedicated vCloud
features and responsibilities related to vApps, VMs and catalogs.

Dedicated vCloud feature responsibility
---------------------------------------

+--------------------------+-----------------------+--------------------------+
| Feature                  | Responsibility        | Description              |
+==========================+=======================+==========================+
| Creating one or more VMs | Customer              | vApps with unmanaged VMs |
| as a vApp                |                       | created from templates   |
|                          |                       | provided by Rackspace.   |
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
| Access to the vCloud API | Customer              | The RESTful vCloud API   |
|                          |                       | used to enable           |
|                          |                       | automation and           |
|                          |                       | integration of           |
|                          |                       | third-party tools into   |
|                          |                       | Dedicated VMware vCloud. |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | vApps created by         |
| customer-provided OVA as |                       | uploading an OVA/OVF     |
| a vApp                   |                       | template into vCloud     |
|                          |                       | Director.                |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | vApp templates created   |
| customer-provided OVA as |                       | by uploading a OVA/OVF   |
| a template in a customer |                       | template into a customer |
| catalog                  |                       | catalog.                 |
+--------------------------+-----------------------+--------------------------+
| Uploading a              | Customer              | ISO files stored in      |
| customer-provided ISO in |                       | vCloud Director by       |
| a customer catalog       |                       | uploading into a         |
|                          |                       | customer catalog media   |
|                          |                       | store.                   |
+--------------------------+-----------------------+--------------------------+
| Read-only access to the  | Customer              | Viewing vCenter          |
| vCenter Server via the   |                       | information with         |
| vSphere API              |                       | read-only permissions    |
|                          |                       | from the vSphere web or  |
|                          |                       | full client, or          |
|                          |                       | third-party software.    |
|                          |                       | (Customer-provided       |
|                          |                       | vSphere plugins are not  |
|                          |                       | supported.)              |
+--------------------------+-----------------------+--------------------------+
| Accessing the vCloud     | Customer              | Using the vCloud         |
| Director user interface  |                       | Director user interface  |
|                          |                       | to operate Dedicated     |
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
|                          |                       | to a different Dedicated |
|                          |                       | vCloud user account.     |
+--------------------------+-----------------------+--------------------------+
| Editing Customer Catalog | Customer              | Editing the properties   |
| Properties               |                       | of a created catalog.    |
+--------------------------+-----------------------+--------------------------+
| Publishing a Customer    | Customer              | Choosing which Dedicated |
| Catalog to another       |                       | vCloud organizations can |
| Organization in the same |                       | access the created       |
| Dedicated vCloud         |                       | catalog.                 |
+--------------------------+-----------------------+--------------------------+
| Sharing a Customer       | Customer              | Selecting users in the   |
| Catalog with other users |                       | Dedicated vCloud         |
| within the same          |                       | organization to use the  |
| Dedicated vCloud         |                       | catalog.                 |
| Organization             |                       |                          |
+--------------------------+-----------------------+--------------------------+
| Creating, modifying, and | Customer              | Create, modify, and      |
| deleting Org Dedicated   |                       | delete independent       |
| vCloud independent disks |                       | disks.                   |
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
| (VCSP) subscription      |                       | two Dedicated vCloud     |
|                          |                       | environments.            |
+--------------------------+-----------------------+--------------------------+
| Creating a customer      | Rackspace             | Creating a customer      |
| catalog that is          |                       | catalog that is          |
| subscribed to an         |                       | subscribed to an         |
| external (VCSP) catalog  |                       | external catalog.        |
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
| Managing Dedicated       | Rackspace             | Managing the Dedicated   |
| vCloud users             |                       | vCloud users and groups  |
|                          |                       | for a customer.          |
+--------------------------+-----------------------+--------------------------+
| Managing Dedicated       | Rackspace             | Creating, modifying or   |
| vCloud external networks |                       | deleting external        |
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
| policies settings -      |                       | organization policies    |
| leases                   |                       | settings - leases as     |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| policies settings -      |                       | organization policies    |
| quotas                   |                       | settings - quotas as     |
|                          |                       | requested by a customer. |
+--------------------------+-----------------------+--------------------------+
| Editing organization     | Rackspace             | Customizing the          |
| policies settings -      |                       | organization policies    |
| limits                   |                       | settings - limits as     |
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
| vCloud                   |                       | vCloud. This is a manual |
|                          |                       | process that requires    |
|                          |                       | down time for the VM.    |
|                          |                       | Windows VMs are not      |
|                          |                       | eligible to move.        |
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
| Dedicated vCloud         |                       | to Dedicate vCloud.      |
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


Dedicated vCloud permissions list
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Customers have the rights to create, delete, and manage VMs within their
Dedicated vCloud. Rackspace manages the vCloud Director Server, vCenter
Server and ESXi hosts. Customers have limited permissions on hosts and
servers. See the Appendix: Dedicated vCloud permissions list for a full
list of permissions.

The following table summarizes Dedicated vCloud permissions.

Dedicated vCloud permissions
----------------------------

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Object
     - Types of Access
   * - Catalog
     - Limited Access
   * - Catalog Item
     - Limited Access
   * - Disk
     - Full Access
   * - General
     - View Only
   * - Group or User
     - View Only
   * - Organisation
     - Limited Access
   * - vApp
     - Limited Access
