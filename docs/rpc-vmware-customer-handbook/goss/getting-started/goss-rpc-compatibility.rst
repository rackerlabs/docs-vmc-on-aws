==================
GOSS compatibility
==================

Guest OS Services for RPC-VMware might not be compatible with all Rackspace
products and services. Contact your Rackspace support specialist for
detailed information about whether any specific Rackspace product is
compatible with your Guest OS Services.

Future development of GOSS automation processes might remove the limitations
referenced in the following sections.

GOSS compatibility with operating systems
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

For a list of supported OS types and versions, refer to the `EOL Terms
<https://www.rackspace.com/information/legal/eolterms>`_ page. For an OS to be
supported for enrollment in Guest OS Services, the OS type and version must be
listed on the page and must not have reached the End-of-Support date indicated.

GOSS compatibility with NSX VxLAN networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you choose to provision NSX VxLAN segments in your RPC-VMware environment,
it will not be possible to enroll VMs that have only NICs connected to VxLAN
segments. A VM must have at least one NIC connected to an Exnet segment in
your environment to enable our systems to provision a public IP address and
NAT on your hosted firewall.

GOSS compatibility with Managed Backup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you choose to restore a VM that was enrolled in GOSS for a purpose other
than direct replacement of the original VM, it will be necessary to request
assistance from your Rackspace support team to either disable or reconfigure
the GOSS with a new VM CMDB identifier. Failure to request this may impact
your support services for the original and/or restored VM.

GOSS compatibility with VM cloning
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you choose to clone a VM that was enrolled in GOSS, it will be necessary to
request assistance from your Rackspace support team to either disable or
reconfigure the GOSS with a new VM CMDB identifier. Failure to request this may
impact your support services for the original and/or cloned VM.

GOSS compatibility with OS IP address changes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you choose to change the local IP address of an enrolled VM, it will be
necessary to request assistance from your Rackspace support team to update the
registered IP Address in our CMDB. Failure to request this may impact your
support services for the VM since the local IP address will no longer be
associated with the public IP NAT that exists on the firewall.

GOSS patching compatibility with customer provided RHEL licensing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Customer provided RedHat OS licenses are not compatible with the GOSS Patching
service for RHEL servers. Since RedHat Licensing is essentially access to RHEL
patches for ongoing maintenance of a server, the customer provided REHL license
(Patching) service would conflict with configuration changes that Rackspace
will make when enrolling a RHEL server VM in GOSS Patching. If you want to
retain your customer provided RHEL licenses, do not select the Patching
service option when enrolling RHEL Server VMs in GOSS.

GOSS compatibility with third-party products
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you choose to implement a third-party solution within your private cloud,
contact the Rackspace account team to explore compatibility with GOSS.
