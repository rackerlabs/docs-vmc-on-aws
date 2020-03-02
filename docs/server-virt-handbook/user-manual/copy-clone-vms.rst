========================
Cloning virtual machines
========================

VMware Server Virtualization offers the ability to clone a VM.
The following table provides an overview of this action.

.. list-table::
   :widths: 50 50
   :header-rows: 1

   * - Description
     - Clone VM
   * - Overview
     - Using the selected VM as a source configuration
       creates one or more running VMs, with a new name and Rackspace
       device number. ``CPU``, ``Memory``, and ``Network`` can be modified
       during the clone process. The VM disk will be identical to the source VM.
   * - Example use case
     - Create a new VM from an existing VM for immediate use.
   * - Requires interaction from the Rackspace VMware Support team.
     - Clone VM does not require manual intervention from the Rackspace VMware
       Support team.

Cloning a virtual machine
~~~~~~~~~~~~~~~~~~~~~~~~~


.. note::

   Initiating this process results in a new billable VM deployed in your
   environment.  Billing commences on the deployment of the VM.

Use the following steps to clone a new virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The virtual machines
   management section displays.

#. Click the selection box next to the virtual machine that you want to clone
   from the virtual machine list.

#. Click ``Clone Selected``.

#. Select the ``Quantity``.

#. Enter the ``Naming Pattern``. This leverages the old name minus the number.
   For example when you clone, ``webserver003``, the naming pattern that is
   presented is ``webserver``. Add the next logical number in the pattern to
   continue the naming pattern.

#. Click ``Configure Clones``. The ``Clone from Existing VM`` page displays.

#. Choose a ``Destination`` (hypervisor).

#. OPTIONAL: If you want, you are now able to update the ``vCPU``, ``Memory``,
   ``Network``, and ``Hard Drive``.

#. Verify the ``Order Details``.

#. Click ``Create clones``.

.. note::

   Rackspace is unable to clone a virtual machine if you are using an
   unsupported operating system or make changes to the recorded Rackspace
   credentials. For more information see :ref:`Credentials Management <svh-credentials-vms>`.
