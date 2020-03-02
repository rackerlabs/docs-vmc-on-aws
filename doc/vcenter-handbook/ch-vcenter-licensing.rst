===============================
Licensing, images, and patching
===============================

This chapter provides the following information:

-  Dedicated vCenter Server licensing

-  Guest Operating System Images

-  Operating System patching

Licensing
---------

This section describes the various licensing options for Dedicated
vCenter Server.

VMware licensing
   You can provide your own VMware licenses, or purchase Rackspace
   provided VMware licenses.

   .. note::
      Licenses cannot be a mixture of your own licenses and licenses
      purchased from Rackspace. They must all be from one source.

   VMware licenses purchased from Rackspace for Dedicated vCenter
   Server are installed during provisioning. Customer supplied VMware
   licenses are applied by Rackspace when Dedicated vCenter Server is
   provisioned. Prior to Rackspace applying a license, a VMware
   installation uses an evaluation license.

Windows OS licensing

   You can provide your own Windows OS licenses or purchase a Rackspace
   provided Windows Data Center license. If you purchased host-based OS
   licensing from Rackspace, it can be activated with the Rackspace KMS
   server. Use the instructions provided by your Rackspace account team.

   .. note::
      The Rackspace KMS server is only accessible to systems hosted with
      Rackspace.

Red Hat OS licensing

   You can provide your own OS licenses or purchase a Rackspace
   provided RHEL host-based license. If you purchased host-based OS
   licensing from Rackspace, it can be activated with the Rackspace RHN
   server. Use the instructions provided by your Rackspace account team.

   .. note::
      The Rackspace RHN server is only accessible to systems hosted with
      Rackspace.

Application licensing
   You will need to provide all application licensing.

Guest Operating System images
-----------------------------

If Rackspace provided OS (Operating System) licensing, Rackspace
provides images to deploy when your initial deployment is complete.
Rackspace does not update the images with patches and updates unless a
specific request is made.

During the initial deployment process, communicate the needed OS images
to your dedicated account team and implementation team. Images are in an
OVA format and will be imported into your storage resources. Images are
uploaded as templates and can be viewed in the VM and Template view.

OS images can be updated by submitting a request to your dedicated
account team. Rackspace will schedule maintenance to disconnect the
existing templates and reconnect new updated templates. During this
maintenance window, accessing the existing templates will cause an
error.

Patching
--------

This section describes how Dedicated vCenter Server is patched.

OS patching
   You can can manage your patches using any external OS patching
   source. You can also opt into the Rackspace OS patching sources for
   RHEL OS. If you run into configuration issues or patching is not
   working, enter a ticket or call your dedicated account team.

VMware patching
   Rackspace will patch the vSphere hosts using VMware vSphere® Update
   Manager™. The vCenter Server will be upgraded as needed as Rackspace
   adds further supported offerings.
