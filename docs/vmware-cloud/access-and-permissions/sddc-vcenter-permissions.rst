
==============================
vCenter access and permissions
==============================

Managed VMware Cloud on AWS customers can use the following options for
vCenter authentication:

* Rackspace-provided Active Directory Service
* Customer-managed Active Directory Service

The preference for the identity source is gathered during the onboarding
process. If the Rackspace-provided Active Directory Service is selected, you
can request adding or removing users through a support ticket. For the
customer-managed Active Directory service, the Active Directory groups for
which vCenter access needs to be granted are specified during onboarding.
The customer can grant access to users by providing membership to specified
group.

**Permissions**

VMware performs the majority of the administration tasks on the
Software-Defined Data Center (SDDC). End users of the service are granted
limited access through the following new roles that are added to the vCenter
user model:

* **CloudAdmin**: The CloudAdmin role has the necessary privileges for you to
  create and manage workloads on your SDDC. However, you cannot access or
  configure certain management components that are supported and managed by
  VMware, such as hosts, clusters, and management virtual machines.
* **CloudGlobalAdmin**: : The CloudGlobalAdmin role is associated with global
  privileges and enables you to perform only certain global tasks, such as
  create and manage Content Library objects.

These roles are granted to the users by membership to a group named
CloudAdminGroup.

For a detailed chart of all of the privileges mapped to these two roles, you
can review the `Privileges Reference for CloudAdmin and CloudGlobalAdmin <https://docs.vmware.com/en/VMware-Cloud-on-AWS/services/com.vmware.vsphere.vmc-aws-manage-data-center.doc/GUID-DFB3C048-5728-4DE9-9380-7240748875C3.html>`_
in the VMware documentation.
