===============================
Configuring vSphere Replication
===============================

VMware vSphere Replication is integrated into the vSphere WebClient,
allowing you to configure and manage replication on a per-VM basis.

To configure replication for a VM use the following steps:

#. Right-click on the VM you want to replicate.

#. Navigate to ``All vSphere Replication Actions``.

#. Select ``Configure Replication``.

#. This brings up the ``Configure Replication`` wizard. Use the
   following settings for each section:

   * Replication type: Replicate to a vCenter Server.

   * Target site: The desired location, typically your target RPC-V
     environment.

   * Replication server: Initially, auto-assign only load balances VMs to
     servers and will not proactively move VMs to new replication servers. You
     can choose to manually select the replication server if you have more
     than one.

   * Target location: Click ``Edit`` to choose the target datastore for the
     VM(s). This can be done per-VM or in bulk. VMware recommends you have 2
     times the available storage at the target side of the VM being
     replicated. If you're using vSAN on the target side, you need to account
     for the protection level (Failures to tolerate [FTT] and Failure
     tolerance method) of the storage policy being applied to the VMDK at the
     target side. For example, if you have a VM consuming 100 GB, a FTT of 1
     requires 400 GB free raw space on the vSAN datastore (100 GB x2 for
     vSphere Replication is 200 GB, FTT1 consumes twice as much on the vSAN
     datastore, thus 400 GB). vSAN displays available raw space without regard
     to FTT or Failure tolerance method because it is applied to the VM level
     and can differ per storage policy. Use the following to determine
     consumption on vSAN:

     * FTT1 with Failure tolerance method of RAID-1 consumes twice (2 times)
       the storage provisioned.

     * FTT2 with Failure tolerance method of RAID-1 consumes triple (3 times)
       the storage provisioned (five-node cluster minimum required).

     * FTT3 with Failure tolerance method of RAID-1 consumes quadruple (4
       times) the storage provisioned (seven-node cluster minimum required).

     * FTT1 with Failure tolerance method of RAID-5/6 consumes one and a third
       (1.3 times) the storage provisioned (four-node cluster minimum
       required).

     * FTT2 with Failure tolerance method of RAID-5/6 consumes one and a half
       (1.5 times) the storage provisioned (six-node cluster minimum
       required).

       .. note::

          If you're using VMFS storage, calculate consumption based on 2 times
          the storage provisioned for the VM.

          This storage requirement is applied to both source and target VMs and
          datastores, as the source site could potentially become the target
          site in the event of a disaster.

#. Replication options

   * Guest OS quiescing (Optional) - This option stuns or pauses the VM during
     a replication process to halt disk modifications in an effort to keep the
     replica consistent. It might impact running services within the guest,
     leverage Microsoft VSS for supported Windows OSs, and might require
     scripts for non-Windows OSs.

   * Network compression (Optional) - This option might reduce throughput
     requirements for replication, but might impact RPO, as there will be
     higher CPU utilization to compress or decompress the data being
     replicated.

#. Recovery point objective (RPO) - The slider does not guarantee RPO and will
   generate a vCenter alert if RPO extends beyond the configured time. We do
   not recommend going below 15 minutes.

#. Point in time instances (Not supported in Managed DR for RPC-V) - You can
   configure the number of snapshots to retain during replication.

   These instances will show up as snapshots on recovered VMs at the target
   site.

   .. warning::

      This can use drastically more storage at the target site as it functions
      similar to a snapshot retaining deltas.

   .. note::

      Snapshot structure on the source-side VMs is not maintained and will be
      consolidated into the multiple point-in-time snapshots on the target
      side VM upon recovery.

#. Monitor vSphere Replication

   #. In the vSphere WebClient, click the home icon and select
      ``Hosts and Clusters``.

   #. Click the vCenter at the top of the left column.

   #. In the middle pane, click ``Monitor`` and then select ``vSphere
      Replication``.

   #. From there, you can select ``Outgoing Replications``, ``Incoming
      Replications``, or ``Reports`` to see additional information.

#. Point in Time (PIT) instances (not supported in Managed DR)

   #. PIT retains replication instances as snapshots post-recovery, providing
      the ability to roll back to previous points in time of a recovered VM.

   #. We do not recommend enabling PIT instances, as this might have
      significant storage requirements and has the potential to fill up the
      datastore at the recovery site.

   #. If you choose to enable PIT instances, be sure to have a minimum of 4
      times the amount (4x) of replicated data in free space at the recovery
      site.
