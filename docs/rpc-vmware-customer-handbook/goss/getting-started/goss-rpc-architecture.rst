=================
GOSS architecture
=================

The following sections describe the systems used with
Guest OS Services (GOSS) for Rackspace Private Cloud powered by
VMware (RPC-VMware). Components are described in the following section.

Automated Systems Interactions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Guest OS Services automation is comprised of a number of systems that interact
with each other to provide the service.

vCenter Indexing
----------------

An automated system is registered with the vCenter Server to receive
vCenter event notifications. These notifications are used to determine when
new Virtual Machines are created in RPC-VMware to make them available
for GOSS enrollment. The system also detects Virtual Machine configuration
changes and when Virtual Machines are deleted.

CMDB
----

Rackspace maintains a CMDB with details about your RPC-VMware environment.
The CMDB is automatically updated with information about the Virtual Machines
that you create in your RPC-VMware environment. The CMDB received additional
updates when you enroll a Virtual Machine in Guest OS Services.

Guest OS Services Automation
----------------------------

Rackspace has created custom automation services to provide the automated
experience for Guest OS Services. This service orchestrates the interactions
between all systems involved in providing Guest OS Services for your Virtual
Machines.

vSphere Guest APIs
------------------

Initial OS access during the enrollment process makes use of the vSphere APIs
for guest actions which requires VMware Tools to be installed and running
within the guest OS. This is used to validate the OS credentials provided with
the enrollment and to ensure that the OS meets the requirements for enrollment.

MyRackspace Portal
------------------

The MyRackspace portal will display your indexed Virtual Machines under
the "Devices" section. This portal is also used when you enroll your
Virtual Machines in Guest OS Services as well as create or interact with
support tickets relating to these systems.

IPAM
----

Rackspace uses an internal IPAM service to keep track of as well as allocate
IP addresses within your RPC-VMware environment. During the automated
enrollment
process, the IPAM service will record the local IP address that you have
assigned
within the Virtual Machine and will provide a public IP address and record the
NAT relationship.

Firewall
--------

Rackspace uses an automation system to perform certain configuration changes
to your
firewall. These changes are limited to adding or removing NAT's on your
firewall
during the automation processes for Guest OS Services.

Ansible
-------

During the automated enrollment process, an Ansible system is used to remotely
execute specific OS actions to perform the required operating system
modifications.

Network Interactions
~~~~~~~~~~~~~~~~~~~~

All automated processes access RPC-VMware management services and Virtual
Machines (VMs) through your hosted firewall.

vCenter Network Interactions
----------------------------

Rackspace automation systems interact with the vCenter server in your RPC-
VMware
environment over a secure connection using a service account that accesses
various functions of the vSphere API.

Direct interactive access of the vCenter Web UI will be used to provide OS
services. This includes observing performance details or accessing the console.

Virtual Machine Network Interactions
------------------------------------

During the enrollment process and at various times after enrollment, the OS of
enrolled VMs is be accessed by Rackspace System Administrators and/or
Automation Systems to perform actions within the guest operating system. The
network access method for enrolled VMs uses dedicated individual public IP
addresses added to the public interface of your hosted firewall. The
public IP is NAT'd to the local IP address of the enrolled VM operating system.

Depending on the OS type of your Virtual Machine, Rackspace uses various secure
network protocols such as ssh, WinRM, and RPD to access the OS.
