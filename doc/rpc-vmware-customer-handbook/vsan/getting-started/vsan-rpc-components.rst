
vSAN components
---------------

vSAN for Rackspace Private Cloud powered by VMware (RPC-VMware)
contains the following components.

.. list-table::
   :widths: 30 70
   :header-rows: 1

   * - Component
     - Description
   * - Host
     - ESXi hosts (hypervisors) run the vSAN software and provide the local
       drives that are used for the cache and capacity tiers.
   * - Disk group
     - A disk group is a unit of physical storage capacity on a host and a
       group of physical devices that provide performance and capacity to
       the vSAN cluster. On each ESXi host that contributes its
       local devices to a vSAN cluster, devices are organized into
       disk groups.
   * - Capacity tier
     - The capacity tier is used to permanently store data that is stored
       in vSAN. Cold data not in the cache tier is written to the capacity
       tier. The capacity tier is made up of flash disks.
   * - Cache tier
     - Each disk group must have one flash cache device and one or more
       capacity devices. The devices used for caching cannot be shared
       across disk groups, and cannot be used for other purposes. A single
       caching device must be dedicated to a single disk group.

       RPC-VMware uses only all-flash clusters. In an
       all-flash cluster, flash devices are used for both the cache tier and
       capacity tier. In all-flash clusters, the cache tier is used to cache
       writes only.
   * - vSAN datastore
     - The datastore that is provided by vSAN and backed by the aggregate
       storage of all drives claimed by vSAN.
   * - VM storage policy
     - VM-level availability and performance policies that can be set and
       modified as needed. vSAN works with VM storage policies to support a
       VM-centric storage approach. If no storage policy is explicitly assigned
       to a VM is when it is provisioned, a generic system-defined storage
       policy called the vSAN Default Storage Policy is automatically applied
       to the VM.
   * - Deduplication and compression
     - Deduplication and compression occur when data is destaged from the
       cache tier to the capacity tier. This function is set when you
       enable “space efficiency” on a cluster level. Deduplication happens
       on a per disk group basis. Bigger disk groups result in a higher
       deduplication ratio. After the blocks are deduplicated, they are
       compressed.
