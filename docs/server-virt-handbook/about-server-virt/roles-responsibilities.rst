.. _svh-roles-and-responsibilities:

==========================
Roles and responsibilities
==========================

The following section defines who is responsible for specific functions
related to managed and unmanaged virtual machines.

If Rackspace is responsible for performing the function, the roles and
responsibilities are designated as ``Rackspace``. If the customer is
responsible for performing the function, the role and responsibilities are
designated as ``Customer``.
 
Because your VMware Server Virtualization environments can be comprised of
both managed and unmanaged virtual machines, VMware Server Virtualization’s
roles and responsibilities are also divided into two sections: managed virtual
machines and unmanaged virtual machines, which includes customer-provided
images.

Managed virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~

VMware Server Virtualization managed virtual machines are virtual machines
that are running a guest operating system that is managed by Rackspace.

The following tables show all of the tasks that Rackspace handles for you
for managed virtual machines and where there is shared responsibility.

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Virtualization
     - Customer
     - Rackspace
   * - Management of underlying virtualization infrastructure
     -
     - ✔
   * - VM container troubleshooting
     - ✔
     - ✔
   * - Remote administration of VMs
     - ✔
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Hardware
     - Customer
     - Rackspace
   * - Manage delivery of equipment
     -
     - ✔
   * - Procure inventory spare parts, and "break-fix" equipment
     -
     - ✔
   * - Provide management of storage (local or external)
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Operating System
     - Customer
     - Rackspace
   * - Provision Rackspace-supported operating systems (MS Windows Server and
       Linux)
     -
     - ✔
   * - Ensure OS licensing compliance
     -
     - ✔
   * - Patch operating systems
     -
     - ✔
   * - Individual file backups (when subscribed)
     -
     - ✔
   * - Maintain password rotation policy for Rackspace credentials
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Monitoring
     - Customer
     - Rackspace
   * - Monitor virtual machine operating systems and applications
     -
     - ✔
   * - Configure monitoring for virtual machine OS and applications
     -
     - ✔
   * - Respond to monitoring alerts for virtual machine OS and applications
     -
     - ✔
   * - Configure and respond to infrastructure monitoring alerts (such as ping
       and port alerts)
     -
     - ✔
   * - Configure and respond to vCenter monitoring alerts
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Network
     - Customer
     - Rackspace
   * - Design, review, and consult on architecture
     -
     - ✔
   * - Configure routing and switching equipment
     -
     - ✔
   * - Allocate IP blocks for guest OS virtual machines
     -
     - ✔
   * - Manage IP blocks assigned for all guest OS virtual machines
     -
     - ✔
   * - Manage firewalls
     -
     - ✔
   * - Manage load balancers
     -
     - ✔
   * - Manage intrusion detection systems
     -
     - ✔
   * - Monitor bandwidth consumption
     -
     - ✔
   * - Troubleshoot network connectivity
     -
     - ✔
   * - Manage firewall rules
     - ✔
     - ✔
   * - Manage virtual machine DNS
     -
     - ✔

Unmanaged virtual machines
~~~~~~~~~~~~~~~~~~~~~~~~~~

VMware Server Virtualization unmanaged virtual machines are virtual machines
that are running a guest operating system that is not managed by Rackspace and
that requires the customer to assume more responsibilities. Unmanaged virtual
machines include customer-provided images. Customers might have a mix of
managed and unmanaged virtual machines running in their VMware Server
Virtualization environment.

The following tables show the tasks for unmanaged virtual machines, with the
customer involved in managing more tasks than with managed virtual machines.

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Virtualization
     - Customer
     - Rackspace
   * - Manage underlying virtualization infrastructure
     -
     - ✔
   * - Troubleshoot container VMs
     - ✔
     - ✔
   * - Remote administration of VMs
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Hardware
     - Customer
     - Rackspace
   * - Manage delivery of equipment
     -
     - ✔
   * - Procure inventory spare parts, and "break-fix" equipment
     -
     - ✔
   * - Provide management of storage (local or external)
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Operating System
     - Customer
     - Rackspace
   * - Provision Rackspace-supported operating systems (MS Windows Server and
       Linux)
     -
     - ✔
   * - Ensure OS licensing compliance
     - ✔
     -
   * - Patch operating systems
     - ✔
     -
   * - Individual file backups
     - ✔
     -
   * - Maintain password rotation policy for Rackspace credentials
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Monitoring
     - Customer
     - Rackspace
   * - Monitor virtual machine operating systems and applications
     - ✔
     -
   * - Configure monitoring for virtual machine OS and applications
     - ✔
     -
   * - Respond to monitoring alerts for virtual machine OS and applications
     - ✔
     -
   * - Configure and respond to infrastructure monitoring alerts (such as ping
       and port alerts)
     -
     - ✔
   * - Configure and respond to vCenter monitoring alerts
     -
     - ✔

.. list-table::
   :widths: 60 20 20
   :header-rows: 1

   * - Network
     - Customer
     - Rackspace
   * - Design, review, and consult on architecture
     -
     - ✔
   * - Configure routing and switching equipment
     -
     - ✔
   * - Allocate IP blocks for guest OS virtual machines
     -
     - ✔
   * - Manage IP blocks assigned for all guest OS virtual machines
     -
     - ✔
   * - Manage firewalls
     -
     - ✔
   * - Manage load balancers
     -
     - ✔
   * - Manage intrusion detection systems
     -
     - ✔
   * - Monitor bandwidth consumption
     -
     - ✔
   * - Troubleshoot network connectivity
     -
     - ✔
   * - Manage firewall rules
     - ✔
     - ✔
   * - Manage virtual machine DNS
     -
     - ✔

Maintenance
~~~~~~~~~~~

To reduce the risk of certain change requests, Rackspace or customers can
recommend that certain functions be performed in a scheduled maintenance. These
scheduled maintenances ensure that the following are available to
the customer:

- Reserved Rackspace resources to complete the defined tasks of the
  maintenance.
- Documented maintenance preparation and quality checks
  from all departments involved in the maintenance.
- Defined length of maintenance to accomplish the defined tasks.
- Documented rollback plan in the event of unforeseen circumstances during
  execution.

Because the full scope of a maintenance cannot be confirmed until all quality
checks have been completed, Rackspace waits until all quality checks have
passed before scheduling.

Scheduling is based on the maintenance calendar availability of all
teams involved and is reserved on a first-come, first-served basis. However, if
this maintenance is urgent or if there is a limited timeline in which to
execute it, contact your account team to see what accommodations can be made.
