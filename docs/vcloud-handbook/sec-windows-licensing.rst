=======================
Windows VM OS licensing
=======================

When a Rackspace-supported Windows VM is deployed from the Rackspace
catalog, the Windows license is automatically activated against the
Rackspace KMS server. If an unsupported Windows VM is deployed from the
Rackspace catalog, it activates with the KMS server but requires manual
configuration.

.. note::

   The Rackspace KMS server is only accessible to systems hosted with
   Rackspace.

Activating a Windows KMS client
-------------------------------

#. Deploy the virtual machine from the provided Windows template.

#. Add the appropriate networking settings to the deployed VM and turn it on.

   .. note::

      If your environment does not have a Dynamic Host Configuration Protocol
      (DHCP) server, add the desired Internet Protocol (IP) to the VM that has
      been assigned to it by your network administrator.

#. Ensure the Domain Name System (DNS) entries are set to the Rackspace DNS
   entries.

   DNS 1: 173.203.4.8

   DNS 2: 173.203.4.9

   .. note::

      If you are not going to refer to Rackspace DNS servers, contact your
      Account Team for a list of appropriate host records to place in your
      internal DNS system.

#. Once the VM is assigned an IP address, type ``ping kms.rackspace.com`` in
   the command line as shown below.

   .. image:: ../figures/licensing-ping-rackspace.png

   .. note::

      You can check the VM’s activation status at this phase by typing
      ``slmgr /xpr`` in the command line.

   .. image:: ../figures/licensing-slmgr-xpr-cmd.png

#. To activate the VM, type ``slmgr /ato`` in the command line.

   .. image:: ../figures/licensing-slmgr-ato-cmd.png

   To check status on activation of the VM, type
   ``slmgr /xpr`` in the command line.

   .. image:: ../figures/licensing-slmgr-xpr-2-cmd.png

#. To set the VM to look for the KMS server on the proper port (1688),
   type ``slmgr /skms kms.rackspace.com:1688`` into a command line
   with elevated privileges.

   .. image:: ../figures/licensing-slmgr-skms-cmd.png

   .. note::

      Your Windows machine is not activated. The machine will automatically
      reach out to the KMS Server and re-activate itself once the expiration
      date and time is met.

Further reading: https://technet.microsoft.com/en-us/library/dn502540.aspx
