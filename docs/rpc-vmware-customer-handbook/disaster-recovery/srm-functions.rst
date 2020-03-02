.. _srm-functions:

===============================
Site Recovery Manager functions
===============================

Test
~~~~

When running a recovery plan in test mode, a snapshot of all VMs associated
to the recovery plan is created and the VM is booted off that snapshot.
SRM imports the VMs and configures the networks based on the network mappings
and recovery plan settings. SRM powers on the VMs based on the configured boot
priority. After every recovery plan run in test mode, you must run a
``Cleanup``.

Cleanup
~~~~~~~

Running the cleanup immediately powers off the recovered VMs and discards all
changed data from the test.

Recovery
~~~~~~~~

In planned migration mode, SRM halts the recovery plan action if any of
the steps fail. SRM attempts data replication to ensure the most recent data
is available. SRM issues a shutdown command to all protected VMS in the
recovery plan.

.. note::

   If any VMs are appliances or do not have VMware Tools, special care needs
   to be made.

Follow the steps in :ref:`VM boot priority <vm-boot-priority>` to configure the
shutdown action for the VM. If this was a previously-run recovery where VMs at
the current source site
were configured to be suspended as part of the recovery, SRM attempts to
resume those VMs. SRM attempts to power on or restore any ESXi hosts at both
sites that might have been powered off by DPM (not supported). SRM
reconfigures the protection group to prepare for migration to the target site.
SRM initiates one more storage replication to ensure the target-side VMs are
in a mirrored state. This insures the guest OS virtual disks are in a clean
state from a graceful shutdown. SRM suspends any non-critical VMs that are
preconfigured to be suspended during a recovery operation. SRM reconfigures
the target-side storage as writeable. SRM imports and powers on the VMs based
on their preconfigured boot priority.

When a recovery plan is run in disaster recovery mode, SRM follows the exact
steps as outlined above, but expects failure. After the source site is back
online, the recovery plan must be run again. SRM steps through any failed steps
and attempts to complete them successfully. You must rerun the recovery plan
until all steps have completed successfully. Once the recovery plan is
successfully listed as ``Recovered``, you *MUST* proceed to run a
``Reprotect``.

Reprotect
~~~~~~~~~

You can only run a ``Reprotect`` after a ``Recover`` has been successfully
completed. In order to reconfigure the protection group and recovery plan to
facilitate failback, you *MUST* run a ``Reprotect``. SRM attempts to power on
any ESXi hosts that have been powered off by DPM (not supported at Rackspace),
and resume any suspended non-critical VMs. SRM reconfigures replication in the
reverse direction. SRM reconfigures the protection group in the reverse
direction. This is where the configuration of reverse mappings is required. See
:ref:`Configuring Site Recovery Manager <configure-srm>`.

IP customization rules going back the other direction are also applied
at this point. SRM begins replication and synchronize the storage.
