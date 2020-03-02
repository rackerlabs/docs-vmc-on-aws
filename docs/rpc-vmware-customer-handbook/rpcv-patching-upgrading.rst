======================
Patching and upgrading
======================

Rackspace periodically patches or upgrades the various Rackspace-provided
services in your RPC-VMware environment. These services are patched or upgraded
to the most recent Rackspace-supported version as needed and to address
critical vulnerabilities.

Rackspace aims to obtain consent before patching or upgrading the
environment to ensure that actions are performed at a convenient time for
you. This process does not require any scheduled downtime for virtual systems
deployed by you in your environment, but it might temporarily impact the
availability of the various user interfaces and APIs of the RPC-VMware
services. The patching or upgrade of hosts might affect the performance of
virtual systems deployed by you in your environment if the patch or upgrade
requires a host to be restarted. Performance should return to normal when
host patching or upgrading is complete.

.. important::
   Rackspace must be able to place ESXi hosts into maintenance mode
   in order to patch your RPC-V environment. Any configuration
   that you create that prevents this may be removed. Speak to
   your support team for more details.
