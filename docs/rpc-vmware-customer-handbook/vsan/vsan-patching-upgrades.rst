===========================
vSAN patching and upgrading
===========================

For details about patching and upgrading, see the
`main patching and upgrading section
<https://developer.rackspace.com/docs/rpc-vmware/rpc-vmware-customer-handbook/rpcv-patching-upgrading/>`_
in the handbook.


vSAN maintenance mode types
---------------------------

The following vSAN maintenance modes can be used on a vSAN cluster during
patching or upgrading. For each type, some impact and use cases information
is provided. Rackspace will coordinate with you to
select the vSAN maintenance mode type that best meets your needs.

Ensure accessibility mode
~~~~~~~~~~~~~~~~~~~~~~~~~

This is the default option. When you power off or remove the host from the
cluster, vSAN ensures that all accessible VMs on this host remain accessible.
Because the host is now absent from the cluster, the vSAN cluster will wait
for one hour, and if the host is not back, rebuild all the components that
were located on the host.

Note that this unprotected state lasts until either the hosts exits
maintenance mode, or after all components located on the hosts have been
rebuilt, which starts one hour after the hosts enters maintenance mode.

Additionally, if a VM goes down because of a component failure while a host
is in this maintenance mode, the VM objects will become available again
when the hosts exits maintenance mode. The VM will most likely have failed
then because it could not access its storage, but it should be possible to
restart the VM.

While the host is in maintenance mode, the cluster lets the VMs in the
cluster that have components stored on the specific host to invalidate
their failure to tolerate (FTT) policy. That is, any VMs in the cluster
with a FTT=1 policy that have components on the host will lose one
component and are therefore not able to tolerate any failure. The VMs
still have enough components to stay up but are not protected from component
failure. If anything else fails in the cluster that stores components of
the VM, the VM's storage is lost and the VM will most likely crash.

Select this option if you take the host out of the cluster temporarily
(for example, to install upgrades) and plan to have the host back in
the cluster. This option is not appropriate when you permanently remove
the host from the cluster.

Full data migration mode
~~~~~~~~~~~~~~~~~~~~~~~~

vSAN evacuates all data to other hosts in the cluster and maintains or
fixes availability compliance for the affected components in the cluster.

This option results in the largest amount of data transfer and consumes
the most time and resources.

The host does not enter maintenance mode if a VM object that has data
on the host is not accessible and cannot be fully evacuated.

Select this option if you plan to migrate the host permanently.

It can also be used to ensure that VMs with the FTT=1 policy don’t have
reduced availability during the maintenance. Note that if the availability
requirements of the VMs are that high, it might be better to use FTT=2
policy instead.

When evacuating data from the last host in the cluster, ensure that you
migrate the VMs to another datastore and then place the host in maintenance
mode.

No data migration mode
~~~~~~~~~~~~~~~~~~~~~~~

vSAN does not evacuate any data from this host.

Any VMs with a FTT value of 1 or higher stay up with reduced availability
(similarly to the Ensure Accessibility option), while any VMs with FTT=0 fail.

This option should be used only during a complete cluster migration, when
all the hosts need to be shut down, and then only after all VMs have been
shut down.
