=============================
Managed Backup for RPC-VMware
=============================

The Managed Backup (MBU) service, which is an add-on component for RPC-VMware,
provides image-based (snapshot) backups of the VMs provisioned in the the RPC-
VMware environment. After configuration, the service backs up all discovered
VMs on a daily basis and retains versions according to the retention policy
that you select. The service also enables image-level restores of an entire VM
so that your workload is recovered as quickly as possible.

The MBU add-on component is not available as a stand-alone product.

.. toctree::
   :maxdepth: 1

   getting-started/index.rst
   mbu-vpc-licensing.rst
   mbu-vpc-patching.rst
   mbu-vpc-api.rst
   using-mbu/index.rst
   mbu-vpc-terms-definitions.rst
