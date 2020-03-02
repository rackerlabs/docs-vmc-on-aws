.. _configure-srm:

=================================
Configuring Site Recovery Manager
=================================

Accessing the Site Recovery Manager interface
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. In the web browser, navigate to the vSphere web client.

#. Log in at the prompt.

   Use either formats: ``DOMAIN\user`` or ``user@domain``.

#. Hover over the``Home`` icon at the top left and click ``Site Recovery``
   from the menu that appears.

#. In the ``Navigator`` pane on the left, click ``Sites``, then click the
   ``local`` site.

#. Enter your credentials in the ``Log In Site`` pop-up for the *target/
   remote* site.

   This allows you to configure SRM for both sites of the pairing from a
   single site.

   .. important::

      If you canceled or closed this dialog box, you will notice an error
      message on the bottom right stating ``The session is not
      authenticated``.

      To authenticate to the target site, click the ``target site`` in the
      ``Navigator``.

#. Click ``Actions`` at the top left of the middle pane and select ``Log In
   Site``.

   .. note::

      Reminder, this is the *target/remote* site credentials, this is
      different from the source site.

#. On the Navigator pane on the left, click the ``local`` site to perform SRM
   actions.

   .. note::

      You may see a warning stating ``No SRAs have been installed``. Disregard
      this warning, as you are using vSphere Replication, which does not
      require an SRA be installed. An SRA is the plugin SRM uses to
      communicate with storage arrays for array-based replication.

Configuring Site Recovery Manager
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Inventory mappings
------------------

Configuring all inventory mappings can be started from the main site interface
within SRM.

#. Log into the vSphere Web client (flash client), mouse-over the ``Home``
   icon for the navigation drop-down menu, then select ``Site Recovery``.

#. From the ``Site Recovery Home`` screen, click ``Sites`` on the left pane,
   then click the ``local`` site name.

#. The ``Summary`` tab has information about the local and paired sites, as
   well as a guide to configure SRM with "Configure inventory mappings" and
   links to the mappings.

#. To view the existing mappings, click the ``Manage`` tab.

   .. note::

      You will need to navigate to the ``Manage`` tab in order to configure the
      ``Storage Policy Mapping``.

To configure the inventory mappings, clicking any of the three options will
open up a wizard that walks you through the mapping process.
The following example is for one option, but note that the process is the same
for the others:

#. From the ``Summary`` tab click ``2.1 Create resource mappings``.

#. There are two modes, leave ``Automatically prepare mappings…`` and click
   ``Next``.

#. This option will find inventory items that are named the same and pre-stage
   the mappings.

#. Select both top level virtual datacenter radio buttons, then click ``Add
   mappings``.

#. SRM browses the hierarchy and map any item with the same name.

   .. note::

      If you have dissimilar names between the source and target, you will need
      to select the manual option and pair up the inventory items
      individually.

#. After you've added all the mappings, click "Next".

   .. important::

      Be sure to click ``Select all applicable`` to create the reverse
      mappings.

      This process only configures only one site (source site to target site),
      so ensure the other site needs the same mappings for failback. This is
      where SRM will automatically create the mappings from the target site
      back to the source site.

#. Click ``Finish``.

   These steps need to be followed for all inventory mappings listed below.


All inventory mappings need to be mapped 1:1 between the source and target
sites to ensure VMs are configured as intended upon failback.

* **Resource mappings**

  This is the location where the VM consumes resources, whether it be a
  cluster or resource pool. Rackspace configures the resource mappings.

* **Folder mappings**

  This is the logical location of the VM in the "VMs and Templates" view.
  You will need to mirror the folder structure at the target site and configure
  the mappings directly to the mirrored folder at the target site. This ensures
  VMs are placed back in their desired folder on fail back.

* **Network mappings**

  Network Mappings is how SRM knows where to logically plug in the VM when it
  is recovered at the target site.

* **Storage Policy mappings**

  Mapping storage policies is crucial and should not be ignored or overlooked.
  If there's no mapping in place, any VM that is recovered at the target site
  will receive the default vSAN storage policy, which could result in using
  as much as 70% additional space inadvertently. Moreover, when a failback
  occurs, all VMs will no longer be assigned their originally assigned
  storage policy.

Placeholder datastore
---------------------

SRM needs to know where to store the placeholder VMs when configuring
protection for VMs. These placeholders are empty containers and only
consume a few kilobytes (KB) of space; this will be vsanDatastore to
vsanDatastore.

.. important::

   These steps need to be performed at both the source and target sites.
   Ensure the steps are completed twice.

#. Re-follow the steps above to get to the ``Summary`` tab and select
   the ``Placeholder Datastores`` tab.

#. Click the icon at the top to create a new placeholder datastore.

   The datastores listed are at the target site in the pop-up window. Check
   the box(es) of the desired datastore(s) and click "OK".

#. Repeat these steps for the other site, using the steps above to navigate
   back to the Site Recovery Home and selecting the other site.

Optional IP customizations
--------------------------

.. important::

   IP Customizations are configured per Network Mapping and must be configured
   at both the source and target sites.

#. Navigate to the ``Manage`` tab within SRM and click the ``Networking
   Mappings`` tab.

#. Select the Network Mapping where the IP Customizations will be needed, and
   click ``Add IP Customization Rule`` to the bottom right of the network
   mapping list.

#. Enter the needed configuration items:

   .. code-block:: console

      Rule name: This should indicate what this rule is for.

      Subnet(s)

      Example:

      Source: 192.168.1.0/24

      Target: 192.168.2.0/24

      The “subnet ID” changes (first three octets in this example), but “host
      ID” does not.

      Gateway: The new default gateway IP at the target site

      DNS Addresses: Enter the IP of the DNS servers at the target site

      DNS suffixes: Enter the DNS search suffixes for the target site

      Primary and Secondary WINS:

#. Click ``OK``.

   Ensure you follow this same process on the other site.

   .. important::

      Keep in mind the new IP Customization Rule you're creating at the target
      site should match the current IP setup of the source site, opposite of
      the rule at the source site.

Protection Groups
-----------------

A Protection Group is the smallest group of VMs, including a single VM, that
can perform a failover at any given time. You can create multiple Protection
Groups, but a VM can be a member of only one Protection group.

A single Protection Group can be a member of multiple Recovery Plans. We
recommend creating a Protection Group based on either application or tier.

Use the following instructions to create a protection group from the vSphere
Web Client (Flash):

#. On the source site, mouse-over the ``Home`` icon and click ``Site
   Recovery`` in the menu that appears.

#. Click ``Protection Groups`` on the left under ``Inventories`` and then click
   ``Create Protection Group.``

#. Enter the following in the dialog box:

   .. code-block:: console

      Name: This needs to be something that differentiates this Protection
      Group from all others.

   .. note::

      Do not name the Protection Group based on the current site as the
      location will change when a recovery is performed.

#. Use the description to elaborate on the name. Click ``Next``.

#. For ``Direction of Protection``, select the source site to target site
   option.

#. Click the option to set the protection group type as ``Individual VMs
   (vSphere Replication)`` and click ``Next``.

#. Select the VMs that you want added to the Protection Group and click
   ``Next``.

   If the VM you intend to protect isn't listed, check the vSphere Replication
   status for that VM, or validate the correct source was selected for
   ``Direction of Protection``.

#. Verify all options are as intended, including the expected total virtual
   machines protected, click ``Finish``.

Recovery Plans
--------------

The Recovery Plan is the list of steps or actions that will be performed for
your Planned Migration or Disaster Recovery. You can have multiple Recovery
Plans with one or more Protection Groups. For example, you can have one
Recovery Plan use the auto networks for test and an identical Recovery Plan
use the live networks (outlined below). A single Protection Group can be a
member of multiple Recovery Plans.

To create a Recovery Plan, follow these steps:

#. Navigate to the Site Recovery Home page as outlined above and click
   ``Recovery Plans`` on the left-hand side under ``Inventories``.

#. Click ``Create Recovery Plan`` and enter the following information in the
   new dialog.

#. Name the Recovery Plan something that differentiates it from any others.

   .. note::

      Do not name the Protection Group based on the current site as the
      location will change when a recovery is performed.

#. Use the description to elaborate on the use of this Recovery Plan and click
   ``Next``.

#. Select the Recovery (Target) site, click ``Next``.

   ``Group type`` should be ``VM protection groups``, check the box(es)
   for the desired Protection Group(s) to be included in the Recovery Plan,
   click ``Next``.

   .. note::

      Special consideration should be taken while configuring the Test
      Networks.

Test networks
^^^^^^^^^^^^^

The Recovery Network is based on the Network Mapping we set up during the
Inventory Mappings process. It is expected that all VMs in the Recovery Plan
will be placed on live production networks during a Recovery operation.

The Test Network defaults to Auto. This is known as the
bubble networks. These bubble networks are isolated to each ESXi host,
as port groups are created for the test without physical network adapter
uplinks assigned. VMs running on the same ESXi host can communicate with each
other, but not outside the host. These special test networks are useful in
validating SRM and storage functionality without impacting any production
networks.

You can set a Test Network to the live network to extend your Recovery Plan
testing to include your application. This is because the VMs will behave the
same as if you're running the Recovery Plan in Recovery mode.

A use-case for creating two Recovery Plans with the same Protection Groups is
to create one with auto networks and one with the live networks. This allows
you to run an SRM test to validate functionality non-intrusively, run a clean
up, and then run the same Recovery Plan in live network mode to validate
application functionality.

When you configure the Test Networks as desired, click ``Next``, then
``Finish``.

.. _vm-boot-priority:

VM boot priority
----------------

There are five (5) boot priorities that can configured per-VM. All VMs default
to a boot priority of 3.

.. important::

   The boot priority is an attribute of the VM and follows it across any and
   all Recovery Plans the VM resides in.

We recommend that you place tiered VMs in different boot priorities to allow
dependencies be met before starting any additional dependent services. All VMs
within the same boot priority start at the same time. SRM does not continue
on to the next boot priority until all VMs are online in the current boot
priority.

To configure VM boot priority, follow these steps:

#. From the Site Recovery Home page in the vSphere Web Client, click
   ``Recovery Plans`` on the left-hand side under ``Inventories`` and click
   the Recovery Plan you want to edit.

#. Click the ``Related Objects`` tab and then the ``Virtual Machines`` sub-
   tab.

#. Select the VM you want to edit and click ``Configure Recovery``.

   The Recovery Properties tab is where you change the Priority Group.

   .. note::

      Managed DR does not support VM dependencies for boot order. For more
      information see `Configure Virtual Machine Dependencies <https://docs.vmware.com/en/Site-Recovery-Manager/6.5/com.vmware.srm.admin.doc/GUID-78869ADE-C1C6-4608-9439-2F0EB069BA44.html>`_.

#. You can override any IP Customization rules that were previously created by
   clicking the ``IP Customization``.

   Alternatively, you can also select the VM in the Virtual Machine list,
   click ``Actions``, ``All Priority Actions``, then select the priority you
   want the selected VM to power on in.

   .. note::

      If you have any appliances or VMs that do not have VMware tools
      installed, you will need to expand ``Startup Actions`` and uncheck the
      checkbox for ``Wait for VMware tools``.

SRM waits for the heartbeat from the VMware tools before marking the VM as
successfully recovered. If there are no VMware tools, SRM assumes the VM did
not recover properly.

Recovery modes
~~~~~~~~~~~~~~

There are two primary modes a Recovery Plan can run in: Test and Run
(as in Run Recovery).

The test mode powers on the VM(s) based on the latest
replicated data from the source site and connects the VMs to the pre-determined
network under the Test Network section of the Recovery Plan. A few things to
note when running a Recovery Plan in Test mode:

* The VM is booted up are crash consistent, meaning they mimic that of a site
  failure as the guest OS was not cleanly shutdown. This is a closer
  representation of how your VMs behave during a Recovery in a disaster.

* VMs running in test mode are similar to VMs running on a Snapshot. When the
  test is cleaned up, the VM is powered off and all changed data is deleted,
  similar to reverting to the snapshot. Any changes made inside the guest OS
  need to be thoroughly documented as the deltas are deleted when the test
  completes.

The run mode is the actual Recovery in the target location, which has two
sub-modes: "Planned migration" and "Disaster recovery".

* Planned Migration is used when both sites are up and running but you want to
  migrate your workloads to the target datacenter. This mode assumes all
  vCenter and SRM services are properly functioning at both sites and will
  fail or halt the Recovery Plan if any step fails or exceeds the expected
  timeout.

* Disaster Recovery mode assumes the source site is offline and will continue
  on error.

You can run a Recovery Plan in test mode many times without impact, only
requiring you to run a clean up to cancel the test.

.. important::

   Clicking ``Run`` on a recovery plan is irreversible and requires you to
   re-run the Recovery Plan until all steps have completed successfully
   before allowing you to run a ``Reprotect`` to allow failback.

   See `Site Recovery Manager functions <srm-functions>` for more information.
