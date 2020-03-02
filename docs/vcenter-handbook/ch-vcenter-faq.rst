===
FAQ
===

**General**

**Q:** How do I access the Dedicated vCenter Server?

**A:** You can access the Dedicated vCenter Server using the java VI
client, vSphere Web Client and the vSphere API. The vSphere hypervisors
(ESXi) are not available for admin access. Any requests for changes to
the hypervisor must be made to Rackspace by opening a Support ticket.

**Q:** How do I know if resources are low?

**A:** Dedicated vCenter Server includes VMware vRealize Operations
(vROps) which has advanced monitoring, forecasting and reporting
capabilities. By viewing the vROps dashboard or by setting certain
alerts, you will be able to know when resources will run out and how
best to optimize and eliminate bottlenecks. Additional third party
software can be installed on a time and materials basis.

**Q:** Are there backups and antivirus agents included?

**A:** The VMware services and managment cluster VMs are protected using
the Dedicated Virtual Machine Recovery (VMR) Virtual Appliance for
backups and antivirus. It is installed and configured using the latest
Rackspace-supported platform. Backups and antivirus are not provided or
supported for any VMs created by you in the compute cluster.

**Q:** How do I migrate my data?

**A:** When migrating data into a Rackspace environment, you can use
VMware vCloud® Connector™, a free tool to move VMs from your on-premise
VMware environment to the Rackspace-hosted Dedicated vCenter Server
environment. Additionally, you can directly upload to a datastore or
import an OVF/OVA-formatted VM. For moving VMs into Dedicated vCenter or
migrating existing virtual machines from a Rackspace Server
Virtualization environment, please contact Rackspace Support.

**Access Control**

**Q:** How are the permissions for users controlled in Dedicated vCenter
Server?

**A:** Rackspace retains admin access to the Dedicated vCenter Server
and vSphere hypervisors. However, over 300 permissions are enabled so
that you can manage the hosted VMs as you would on-premise. If you need
more access, it will be handled on a case-by-case basis to ensure that
the requested permission does not put the health of the environment at
risk.

**Q:** Can I use the same login information if I have multiple Dedicated
vCenter Servers in a single data center?

**A:** Each vCenter is deployed autonomously, so each will have its own
set of accounts. Rackspace can provide a single authentication source
for all environments (for example, Rackspace Intensive Domain).

**Q:** Is the Dedicated vCenter Server a VM or is it dedicated hardware?

**A:** The Dedicated vCenter Server is a VM appliance. Additional VMware
services are also be installed as VMs.

**Q:** Which edition of Microsoft SQL Server is used?

**A:** The vCenter Server uses an embedded Postgres database. The
vSphere Update Manager server uses a SQL database.

**Q:** Can I manage the vSphere hypervisors (ESXi) if I have Dedicated
vCenter Server?

**A:** No. You will not have direct access to the vSphere hypervisor and
thus cannot manage it. All hypervisor change requests will need to be
made to Rackspace by submitting a Support ticket.

**Q:** Can I add vSphere hypervisors (ESXi) in my on-premise data center
to the Dedicated vCenter Server in a Dedicated vCenter Server
environment?

**A:** This is currently not supported. Only vSphere hypervisors hosted
at Rackspace as part of the Dedicated vCenter Server environment can be
managed by the Dedicated vCenter Server.

**Q:** With Dedicated vCenter Server, do I have full control over ESXi
hypervisors to import/export my own VMs?

**A:** You have full import and export capability of your VMs. However,
Rackspace-provided images will not work outside of the Rackspace data
center.

**Q:** Can I manage the Dedicated vCenter Server plugins and add my own
third-party plugins?

**A:** You can instal Rackspace endorsed plugins. Rackspace does not
support or configure anything that Rackspace is not actively using. The
support of endorsed plugins is limited to install and basic
configuration.

**Q:** What kind of Single Sign-On (SSO) capabilities can we use?

**A:** By default, your Dedicated vCenter Server authenticates against
the Rackspace Intensive Domain. If you want to add your domain as
another authentication source, then Rackspace can add it into the VMware
SSO service.

**Architecture**

**Q:** Can I connect the Rackspace hosted Dedicated vCenter Server to a
Dedicated vCenter Server in a different data center?

**A:** No. Enabling Link Mode across any appreciable distance is not
supported due to networking latency concerns. For specific requests,
submit a ticket to Rackspace Support.

**Q:** Which modules are included with Dedicated vCenter Server?

**A:** vCenter Server with VMware Infrastructure (VI) Client, vSphere
Web Client, vSphere (API access), Dedicated Virtual Machine Recovery
(VMR) backup appliance, vRealize Operations (vROps) appliance and VMware
Update Manager (VUM) appliance is included. Additional services outside
the core offering (for example, unsupported 3rd-party tools that require
administrator permissions) can be installed on a time and materials
basis, but are not be covered by the SLA.

**Q:** Are automation APIs and VMware vSphere PowerCLI available?

**A:** Yes, but the permissions, as they are set, may not allow certain
actions.

**Q:** Is Dedicated vCenter compatible with third-party products?

**A:** In the future, Rackspace may certify third-party products for use
with Dedicated vCenter Server. Rackspace will provide details about the
compatibility level and requirements as they become available.

**Q:** Can I install a third-party tool that requires elevated permissions?

**A:** In some cases, existing role permissions provided by Rackspace
do not allow a custom or third-party tool to function. Contact the
Rackspace Virtualization Team to determine if role permission
adjustments are possible.
