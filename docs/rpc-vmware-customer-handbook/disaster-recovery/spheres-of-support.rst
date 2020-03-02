==================
Spheres of support
==================

The Disaster Recovery add-on for Rackspace Private Cloud powered by VMware
comes in two levels: Essential and Managed. Both levels are deployed with the
same components and only differ only in how they are supported by Rackspace.

Essential
~~~~~~~~~

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * -
     - Rackspace
     - Customer
   * - vSphere Replication deployment
     - ✔
     -
   * - vSphere Replication site pairing
     - ✔
     -
   * - SRM service monitoring
     - ✔
     -
   * - SRM installation
     - ✔
     -
   * - SRM site pairing
     - ✔
     -
   * - SRM inventory mappings(1)
     - ✔
     - ✔
   * - SRM placeholder datastore
     - ✔
     -
   * - vSphere Replication - configure VM replication
     -
     - ✔
   * - vSphere Replication - service monitoring
     - ✔
     -
   * - vSphere Replication - monitor RPO
     -
     - ✔
   * - vSphere Replication - monitor VM status
     -
     - ✔
   * - vSphere Replication - stop VM replication
     -
     - ✔
   * - SRM - configure VM protection
     -
     - ✔
   * - SRM - configure VM boot priority
     -
     - ✔
   * - SRM - configure IP customization rules
     -
     - ✔
   * - SRM - configure protection groups
     -
     - ✔
   * - SRM - configure recovery plans
     -
     - ✔
   * - SRM - run recovery plan in test mode(2)
     -
     - ✔
   * - SRM - run recovery plan in planned migration mode(2)
     -
     - ✔
   * - SRM - run recovery plan in disaster recovery mode(2)
     -
     - ✔
   * - SRM - add VM to protection group
     -
     - ✔
   * - SRM - add VM to recovery plan
     -
     - ✔
   * - SRM - remove VM from protection group
     -
     - ✔
   * - SRM - remove VM from protection group
     -
     - ✔

#. Customer-created logical switches might need to be mapped to the recovery
   site.

#. Additional Rackspace teams might need to be involved during Recovery Plan
   operations.

Managed
~~~~~~~

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * -
     - Rackspace
     - Customer
   * - vSphere Replication deployment
     - ✔
     -
   * - vSphere Replication site pairing
     - ✔
     -
   * - SRM service monitoring
     - ✔
     -
   * - SRM installation
     - ✔
     -
   * - SRM site pairing
     - ✔
     -
   * - SRM inventory mappings(1)
     - ✔
     -
   * - SRM placeholder datastore
     - ✔
     -
   * - vSphere Replication - configure VM replication
     - ✔
     -
   * - vSphere Replication - service monitoring
     - ✔
     -
   * - vSphere Replication - monitor RPO
     - ✔
     -
   * - vSphere Replication - monitor VM status
     - ✔
     -
   * - vSphere Replication - stop VM replication
     - ✔
     -
   * - SRM - configure VM protection
     - ✔
     -
   * - SRM - configure VM boot priority
     - ✔
     -
   * - SRM - configure IP customization rules
     - ✔
     -
   * - SRM - configure protection groups
     - ✔
     -
   * - SRM - configure recovery plans
     - ✔
     -
   * - SRM - run recovery plan in test mode(2)
     - ✔
     - ✔
   * - SRM - run recovery plan in planned migration mode
     - ✔
     -
   * - SRM - run recovery plan in disaster recovery mode(2)
     - ✔
     - ✔
   * - SRM - add VM to protection group
     - ✔
     -
   * - SRM - add VM to recovery plan
     - ✔
     -
   * - SRM - remove VM from protection group
     - ✔
     -
   * - SRM - remove VM from protection group
     - ✔
     -

#. If required, notify Rackspace of any customer-created logical switches to
   create the network mapping.

#. Additional Rackspace teams might need to be involved during recovery plan
   operations.
