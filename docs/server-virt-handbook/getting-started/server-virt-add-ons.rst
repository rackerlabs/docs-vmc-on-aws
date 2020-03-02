===============
Add-on services
===============

The following sections detail the architecture, features, terms
and conditions, and the roles and responsibilities for the following
VMware Server Virtualization Disaster Recovery (DR) add-ons:

.. toctree::
   :maxdepth: 1

   replication-manager.rst
   vm-replication.rst
   vm-recovery.rst

Add-on services comparison
~~~~~~~~~~~~~~~~~~~~~~~~~~

Although these add-on services have similar names and purposes,
they differ in the following ways:

.. list-table::
   :widths: 16 28 28 28
   :header-rows: 1

   * - Characteristic
     - VM Replication
     - Replication Manager
     - VM Recovery
   * - Purpose
     - Data replication per VM for disaster recovery (DR)
     - Data replication and managed VM recovery plan
     - Backup and recovery
   * - Recovery scenarios
     - Partial to entire data center failure
     - Partial to entire data center failure
     - Local failures / operational recovery
   * - Recovery Location
     - Recovery to secondary (DR) data center
     - Recovery to secondary (DR) data center. (But the role of the protected
       and secondary data centers and the direction of the replication can be
       periodically reversed)
     - Recovery to the production data center
   * - Replication technology
     - Software based
     - Storage based replication
     - N/A
   * - Requires dedicated storage
     - No
     - Yes
     - No
   * - Recovery time SLA
     - No
     - Yes
     - Guaranteed response time to initiate restor (2 hour for onsite data)
   * - Recovery Point Objective (RPO)
     - 4 hours
     - 1 hour
     - 24 hours
   * - VM Protection Groups
     - No
     - Yes
     - N/A
   * - Pre-defined recovery plan with specific boot order
     - No
     - Yes
     - N/A
   * - MyRackspace portal Integration
     - No
     - Yes
     - Yes
   * - Additional VM Cost
     - No
     - Yes
     - Yes
   * - Number of VMs supported
     - 40
     - Hundreds
     - No VM Recovery specific limit
