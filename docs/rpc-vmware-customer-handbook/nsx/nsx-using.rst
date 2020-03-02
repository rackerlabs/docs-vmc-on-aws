========================
Using NSX for RPC-VMware
========================

If you want to add individuals or groups to NSX roles,
the NSX Enterprise Administrator must add them to the NSX roles
through the NSX permissions section in the vSphere web client.

Rackspace configures NSX and the underlying infrastructure so
that you can begin to tailor the NSX environment to your
needs. Rackspace follows VMware best practices by deploying three NSX
controllers for the environment. VMware only supports the use of only three
controllers, even though it is possible to add and subtract controllers.
If you remove or add NSX controllers, you will be outside of VMware's and
Rackspace’s support requirements.

.. caution::

   It is possible for you to create Distributed
   Firewall rules that could block all traffic in and out of the VMs. Take
   extra care when creating these types of rules in NSX.
