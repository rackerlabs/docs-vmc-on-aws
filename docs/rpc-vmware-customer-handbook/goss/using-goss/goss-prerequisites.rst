=======================
Enrollment requirements
=======================

Before a VM can be enrolled in Guest OS Services, it must meet the following
requirements:

.. note::
   Rackspace encourages the use of the Rackspace complementary VM templates
   when
   deploying VMs that will be enrolled in Guest OS Services. Rackspace OS
   Administrators
   are accustomed to the operating system configurations of these VM templates.

General requirements
~~~~~~~~~~~~~~~~~~~~

- The VM OS must be a supported type and version.
- VM is powered on.
- VMware Tools version 10.x is installed and running.

.. note::
   We recommended that the latest supported version of VMware tools is
   installed
   for best results during the automated enrollments.

- The OS of the VM must have the local firewall disabled and allow remote
  access and
  privileged process execution by the enrollment account.
- Two Factor Authentication (2FA) must not be enabled for the enrollment
  account or the
  ``rack`` user account created during the enrollment process.
- The VM must have at least one NIC connected to a physical network with at
  least one IPv4 IP address configured that matches the physical network
  topology.

.. note::
   Guest OS Services does not support IPv6 addresses. You must disable IPv6
   before
   enrollment in Guest OS Services.

Windows requirements
~~~~~~~~~~~~~~~~~~~~

OS administration
-----------------

- PowerShell v3 or higher must be installed.

  .. note::
     If MaxMemoryPerShellMB quota is increased for PowerShell v3, you must
     apply
     hotfix 2842230 or update to a newer version of PowerShell. If applying
     the hotfix,
     MaxMemoryPerShellMB should be set to 2048.

- You must disable User Account Control (UAC) for all users that are members
  of the local
  Administrators group.
- WinRM must be able to start and TLS 1.2 must be enabled.
- An Administrator-privileged login for remote access must be provided for
  enrollment.
- Remote Desktop sessions must be enabled.
- For servers joined to customer Active Directory, AD DNS service must be
  configured with Rackspace DNS forwarders. Contact your account team
  for details.

.. note::
   For servers joined to customer Active Directory, any group policy settings
   active for the servers being enrolled in Guest OS Services must not conflict
   with or revert any of the changes being made during or after enrollment.

Linux requirements
~~~~~~~~~~~~~~~~~~

OS administration
-----------------

- Remote SSH logins for the user credential provided must be allowed.
- A root privileged login must be provided for enrollment.
- A valid repo must be configured for dependent package installation.
- All invalid repo references should be removed, including original ISOs used

.. note::
   The valid repo requirement does not apply if Rackspace patching is selected.

Patching
--------

- Customer-provided RHEL licensing must not be in use. If the patching service
  is selected, the Rackspace patching service is configured instead of
  the existing patching service subscription.
- CentOS servers must have rhn packages installed to qualify for enrollment of
  the
  patching service. Verify that the following packages are installed:
  ``rhn-client-tools rhn-check rhn-setup rhnsd m2crypto yum-rhn-plugin``
