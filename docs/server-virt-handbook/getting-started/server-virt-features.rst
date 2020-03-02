=====================================
VMware Server Virtualization features
=====================================

The following table describes the features that are available to you as a
VMware Server Virtualization customer, based upon your configuration and
subscriptions.

.. list-table::
   :widths: 30 70
   :header-rows: 1

   * - Features
     - Description
   * - vMotion®
     - VMware VMotion enables the live migration of running virtual machines
       from one physical server to another with zero downtime, continuous
       service availability, and complete transaction integrity.
   * - Storage vMotion
     - Storage vMotion is a component of VMware vSphere that allows live
       migration of a running VMs file system from one
       storage system to another. While most customers will not see the
       disruption, performance degradation is possible, especially if
       the VM is busy. This migration occurs while maintaining data
       integrity.
   * - vSphere High Availability (HA)
     - VMware HA provides high availability for virtual machines by pooling
       them and the hosts that they reside on into a cluster. Hosts in the
       cluster are monitored and in the event of a failure, the virtual
       machines on a failed host are restarted on alternate hosts.
   * - VMware snapshots
     - Snapshots allow you to safely commit changes and roll back updates to
       your VMs by saving snapshots of your VMs prior to changes.
   * - vSphere Distributed Resource Scheduler (DRS)
     - VMware DRS is a utility that balances
       computing workloads with available resources in a virtualized
       environment.
   * - Performance graphs
     - Within the MyRackspace portal, customers can view statistics that make
       it easy to determine your available compute capacity (CPU, disk, and
       memory) and any compute constraints caused by resource-intensive VMs.
   * - Access via portal
     - Customers have access to the VMware Server Virtualization section in
       the MyRackspace Web Portal to administer their hosted environment and
       resources. For more details, see
       :ref:`Managing virtual machines <svh-manage-vms>`.
   * - File-level backups and restore
     - Fully-managed backup service where customers interact via the
       MyRackspace portal. Customers can view their configuration, backup
       status, and history.
       Customers are also able to submit change requests and restore requests
       via the MyRackspace portal.

       .. important::

          Snapshots consume additional space on the underlying storage and
          grow over time in the background, sometimes rapidly. We advise that
          you delete snapshots as soon as they are no longer needed. If the
          underlying datastore runs out of space, you can experience downtime,
          performance degradation, or some VMware features may not work as
          expected.

VMware Server Virtualization managed services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Below are the managed services that Rackspace provides VMware Server
Virtualization customers.

.. list-table::
   :widths: 30 70
   :header-rows: 1

   * - Area
     - Managed by Rackspace
   * - Virtualization
     -
       - Management of VMs and appliances
    
       - Remote administration of VMs
    
       - VM troubleshooting
    
       - Guest OS patching
    
       - Anti-virus updates (when subscribed)
    
       - Managed backups (when subscribed)
   * - Hardware
     -
    
       - Manage delivery of equipment
    
       - Procure, inventory spare parts, and break-fix equipment
    
       - Rackspace Fully Managed Dedicated NAS (when added)
    
       - Rackspace Fully Managed Dedicated SAN (when added)
    
       - Rackspace Fully Managed Shared SAN (when added)
   * - Network
     -
    
       - Architecture design, review, and consultation
    
       - Configure physical routing and switching equipment
    
       - Allocate public and private IP blocks for guest OS VMs
    
       - Manage physical firewalls
    
       - Manage physical load balancers

       - Manage physical intrusion-detection systems
    
       - Monitor bandwidth consumption
    
       - Troubleshoot network connectivity
    
       - Manage physical firewall rule set (co-managed with customer)
   * - Monitoring
     -
    
       - Configure and respond to infrastructure monitoring

       - Configure and respond to datastore space thresholds
    
       - Provide, configure, and respond to monitoring of the OS and
         applications on compute VM
    
       - Notification preferences for ticketing and email alerts

Patching and upgrading
~~~~~~~~~~~~~~~~~~~~~~

VMware Server Virtualization provides VMware ESXi and OS patching.

ESXi patching
-------------
 
Rackspace works with customers to perform VMware ESXi upgrades at their
request or to address critical vulnerabilities. 
 
Because customers' VMware Server Virtualization configuration can vary, we
recommend reaching out to your account team to discuss upgraded options
that best suit your environment and needs.
 
OS patching
-----------
 
Rackspace provides a managed OS patching service for supported operating
systems. Rackspace tests all patches in lab-environments before applying
monthly to customer environments. The patching schedule is agreed upon
by the customer.

.. note::

   The monthly testing schedule refers only to guest OS.
