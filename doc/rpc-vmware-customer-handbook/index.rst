===========================================================
Rackspace Private Cloud powered by VMware Customer Handbook
===========================================================

Rackspace Private Cloud powered by VMware (RPC-VMware) enables a
VMware Software-Defined Data Center (SDDC) as a single-tenant private
cloud that conveniently transitions or extends your on-premises VMware
workloads into a hosted VMware environment. It is built on top of the
standard VMware virtualization and software-defined technologies:

* VMware vSphere®
* NSX™
* vSAN™,
* The vRealize® Suite.

RPC-VMware is available not only in a Rackspace data center but also in
the customers own or 3rd party data centers.

This handbook is your primary resource for information related to
RPC-VMware, including chapters on how to get started, using RPC-VMware, and
how to get help. It also includes additional resources that are external to the
handbook.

.. toctree::
   :maxdepth: 1

   rpcv-getting-started.rst
   rpcv-core-components.rst
   rpcv-licensing.rst
   rpcv-patching-upgrading.rst
   rpcv-using.rst
   rpcv-add-ons.rst
   rpcv-managed-services.rst
   rpcv-additional-resources.rst
   disclaimer-link.rst

RPC-VMware versus Server Virtualization
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. list-table::
   :widths: 20 40 40
   :header-rows: 1

   * - Feature
     - VMware Server Virtualization
     - Rackspace Private Cloud Powered by VMware
   * - Managed support for VMware stack and underlying hardware
     - Yes
     - Yes
   * - Managed Guest OS-layer support (For example, OS patching)
     - Yes
     - No
   * - Hosted catalogs
     - No
     - Customer Provided OS, and Rackspace Provided OS with Host based
       licensing (Optional)
   * - Access via API
     - None
     - vSphere® API, NSX API, vSAN API, vRealize Operations Manager API, and
       vRealize Automation API (Optional)
   * - Access via GUI
     - MyRackspace® Web Portal
     - vSphere® Web Interface, vRealize Operations Web Portal, and vRealize
       Automation Web Portal (Optional)
   * - Single-tenant vSphere hypervisors
     - Yes
     - Yes
   * - Storage options
     - Local disk, DAS, SAN, Dedicated EMC SAN, and NetApp NAS
     - SAN, Dedicated EMC SAN, NetApp NAS, and VMware vSAN
   * - Networking options
     - Brocade, F5, and Cisco
     - Brocade, F5, Cisco, and NSX Software-Defined Networking
   * - Service level options
     - Managed and Intensive SLA
     - Intensive SLA
   * - Compatible with VMware vRA
     - No
     - Yes
   * - Capacity planning
     - Rackspace assistance provided
     - VMware vROps included
   * - Availability in customer's or 3rd party data center
     - No
     - Yes

If you want to learn more about the VMware Server Virtualization offering,
see the `VMware Server Virtualization Customer Handbook <https://developer.rackspace.com/docs/docs-vmware-server-virt/server-virt-handbook/>`_.
