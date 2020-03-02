.. _vrops-permissions:

vRealize Operations roles and permissions
-----------------------------------------

Rackspace completely manages and supports the vRealize Operation appliance,
including the following tasks:

-  Keeping the vRealize Operations appliance and its embedded services up
   and running

-  Backing up and restoring the appliance as needed

-  Installing supported management packs

Customers are expected to self-manage the custom reports, dashboards,
alerts, and other items that they create in vRealize Operations. Customers are
also responsible for installing Endpoint Operations agents.

To implement the separation of customer and Rackspace duties in vRealize
Operations, Rackspace implements vRealize roles. Customers are assigned the
vRealize Operations PowerUserMinusRemediation role and have privileges to
perform all of the same actions as those who are assigned the Administrator
role, except for user management, cluster management, and remediation actions.

The following table identifies the privileges that are *not* assigned to
the PowerUserMinusRemediation role.

.. list-table::
   :widths: 30 30 40
   :header-rows: 1

   * - Privilege category
     - Privileges
     - Impact
   * - Administration - Access control
     -
       -  Add, edit, or delete a role
       -  Manage object permission for user
       -  Manage user related operations
       -  Update password policy
     - The user can view but cannot configure access control for other users.
       For example, the user cannot delegate or limit access to other users in
       the vRealize Operations environment.
   * - Administration – Manage AuthSources
     - Configure AuthSources
     - The user can view but cannot configure authentication sources. For
       example, the user cannot add an Active Directory domain as
       authentication source in the vRealize Operations environment.
   * - Administration – Manage cluster
     - All administrative actions
     - The user can view but cannot perform any administration actions on
       the cluster. For example, the user cannot add new vRealize Operations
       nodes to the cluster.
   * - Administration – REST APIs
     - Delete alert note
     - The user can use REST APIs to perform all provided activities except
       delete alert notes.
   * - Content
     -
       -  Manage heat map configurations
       -  Manage plug-ins
     - The user can manage all content except heat map configurations
       and plug-ins.
   * - Environment
     - Action
     - The user cannot perform any of the out-of-the-box actions. For example,
       the user cannot use the Power Off VM or Migrate VM actions in
       the vRealize Operations environment.
   * - Environment – Alert notes management
     - Delete
     - The user can add but cannot delete alert notes.
