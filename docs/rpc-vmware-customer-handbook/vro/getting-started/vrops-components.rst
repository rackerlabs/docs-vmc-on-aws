.. _vrops-components:

vRealize Operations components
------------------------------

The vRealize Operations virtual appliance is registered with VMware vCenter®
and collects metrics from the vCenter objects.

Management packs
~~~~~~~~~~~~~~~~

Management packs are add-ons to vRealize Operations that are installed by
Rackspace. They extend the capabilities of the metrics collected by
vRealize Operations for applications and systems that are not metered by the
default vRealize Operations installation.

The following set of management packs are installed in vRealize Operations
by default:

-  Management Pack for vSAN

-  Management Pack for NSX for vSphere

-  Management Pack for SDDC Health


Endpoint Operations Managment agents
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Endpoint Operations Management agents are enabled by a management pack that
you can install in the OS of VMs to collect specific metrics that are fed
to management packs in vRealize Operations. The agents are Java-based agents
that are installed directly on the VM. The agents feed metrics to the
vRealize Operations appliance, which enables a deeper view into objects or
applications.

The Endpoint Operations Management agents use Java. If you
have an application that depends on a certain version of Java, take this into
consideration when you are deciding whether to install the Java agent or
the non-Java agent.
