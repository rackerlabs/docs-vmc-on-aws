=====================
Site Recovery Manager
=====================

VMware Site Recovery Manager (SRM) is a business continuity and disaster
recovery (DR) solution that helps you to plan, test, and run the recovery of
virtual machines between a protected vCenter Server site and a recovery
vCenter Server site. You can use SRM to implement different types of recovery
from the protected site to the recovery site.

#. Planned migration is the orderly evacuation of virtual machines from the
   protected site to the recovery site. Planned migration prevents data loss
   when migrating workloads by replicating storage before and after shutting
   down all VMs and bringing them up on the recovery site. For a planned
   migration to succeed, both sites must be running and fully functioning.

#. Disaster recovery does not require that both sites be up and running, for
   example if the protected site goes offline unexpectedly. During a disaster
   recovery operation, failure of operations on the protected site is reported
   but is otherwise ignored. After the protected site is online, re-running
   the recovery plan allows the sites to reestablish their connection and any
   failed recovery steps are rerun.

.. toctree::
   :maxdepth: 1

   configuring-srm.rst
   srm-functions.rst

Planning
~~~~~~~~

#. What apps should you protect?

   * Business critical apps: Applications or servers that are essential to
     your company's operation. Resist putting too many in this category to
     start with.

   * Tier the applications and the supporting infrastructure to decide which
     should be recovered first.

   * Remember not everything will be needed in disaster recovery. Some VM’s
     can be left out and restarted once the primary site is back online.

#. Where and how should you recover applications?

   * Running Active/Active is often the preferred method. This allows for your
     applications to continue to run even if you lose one site. Running an
     Active/Passive method allows you to reduce the footprint of your
     target location if you intend to run less VMs or a higher consolidation
     ratio.

   * In either method, you can use the idle resources to run your test,
     development, or certification environment.

#. Vendor support

   * Before configuring SRM, you should consult with the software vendor to
     ensure supportability of the software by the vendor in the event of
     an SRM recovery operation.

#. IP customizations

   SRM has the ability to change in-guest IP addresses based on subnets.
   This is a powerful tool to change subnets to match the target-side IP
   subnets.

   * Pros:

     * There is no requirement to stretch layer 2 subnets across sites
       (some network devices are incapable of this function, such as Cisco's
       ASA).

     * Allows all network subnets to be up and available at all times.

   * Cons:

     * When the OS boots and VM tools check in with vCenter, SRM will re-IP
       the guest OS and issue a reboot command, extending your recovery time.

     * Might require application-specific connections to be modified for the
       new IP address.

     * SRM cannot change IPs on virtual appliances without VM tools.

#. If you have the same subnets on both sites, you might not need to leverage
   this tool and can leave the in-guest IPs the same on either site.

   * Pros:

     * There is no requirement to reconfigure application connections during a
       recovery.

     * Recovery times are faster as there isn't a subsequent reboot post-IP
       change.

   * Cons:

     * The subnet on the target side will need to be shut to allow proper
       routing between the environments, requiring NetSec to not shut the
       subnet for testing or recovery.

     * Recovery might happen quickly, but VMs will be isolated until network
       connectivity is restored.

       .. note::

          This relates to in-guest IP addresses only and does not change
          public IP addresses
