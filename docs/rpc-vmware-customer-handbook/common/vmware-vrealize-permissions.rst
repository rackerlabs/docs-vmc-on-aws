:orphan:

================
Permissions list
================

Dedicated VMware® vCenter Server™, and Rackspace Private Cloud powered
by VMware vCloud® customers are assigned the VMware vRealize Operations
(vROps) ``PowerUserMinusRemediation`` role and have privileges to
perform all of the same actions as those who are assigned the
Administrator role, EXCEPT for user management, cluster management or
remediation actions.

The following table identifies the privileges that are NOT assigned to
the ``PowerUserMinusRemediation`` role.

.. list-table::
   :widths: 30 35 35
   :header-rows: 1

   * - Privilege category
     - Privileges
     - Impact
   * - Administration - Access Control
     - Add, Edit or Delete a Role, Manage Object Permission for User, Manage
       User Related Operations, Update Password Policy
     - The user can view, but cannot configure access control for other users.
       For example, the user cannot delegate or limit access to other users in
       the vROps environment.
   * - Administration – Manage Auth- Sources
     - Configure AuthSources
     - The user can view, but cannot configure authentication sources. For
       example, the user cannot add an Active Directory domain as
       authentication source in the vROps environment.
   * - Administration – Manage Cluster
     - All Administrative Actions
     - The user can view, but cannot perform any administration actions on the
       cluster. For example, the user cannot add new vROps nodes to the
       cluster.
   * - Administration – REST APIs
     - Delete Alert Note
     - The user can use REST APIs to perform all provided activities, except
       delete alert notes.
   * - Content
     - Manage Heat Map Configurations, manage Plug-ins
     - The user can manage all content, except heat map configurations and
       plug-ins.
   * - Environment
     - Action
     - The user cannot perform any of the out-of-the-box actions. For example,
       the user cannot use the Power Off VM or Migrate VM actions in the vROps environment.
   * - Environment – Alert Notes Management
     - Delete
     - User can add, but cannot delete alert notes.
