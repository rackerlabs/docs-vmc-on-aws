.. _svh-manage-vms:

=========================
Ordering virtual machines
=========================

This section takes you through the steps for creating one, or multiple,
virtual machines.

.. important::

   Before you begin, ensure you are on the ``Dedicated Hosting`` tab on the
   top right-hand corner of your browser.

   ``Dedicated Hosting`` is highlighted in red if you are in the
   correct tab.

Creating a new virtual machine
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   .. note::

      This creates a new, fresh VM. If you want to create a new
      VM as a clone of one of your existing VMs, see the ``Cloning a virtual
      machine`` section. This copies all the virtual hardware specifications,
      operating system, and data from your existing VM of your choosing.

Use the following steps to create a new virtual machine:

#. Click the ``Products`` dropdown menu.

#. Select ``VMware Server Virtualization`` from the list. The Virtual Machines
   management section displays.

#. Click ``Order Virtual Machine`` on the center panel. This navigates to the
   ``New Virtual Machine`` order form.

#. Select the `Hypervisor` or `Cluster` from the ``Deployment Destination``
   dropdown menu.

   .. note::

      Based on your selection, the rest of the form takes a moment or two to
      populate.

#. Select an OS for the VM from the ``Image`` list available

#. Scroll to the ``Configuration`` section. Allocate the desired ``vCPU``,
   ``vRAM``, and ``Network``.

#. Scroll to the ``Storage`` section. Select the ``Root Storage Device``,
   ``Root Storage Size``, and the ``Root Mountpoint``.

   .. note::

      The ``Root Mountpoint`` can auto-allocate, depending on your selection.

   Add any additional storage required by clicking ``Add Storage``

#. Scroll to the ``Identification`` section and name the new virtual machine.
   It must be a Fully Qualified Domain Name (FQDN), Top Level Domain (TLD), or
   ``.local host name``.

   .. note::

      The complete Virtual Machine name must be 6 to 70 characters long.
      If you are creating a Windows-based VM, the host
      name itself cannot be longer than 8 characters.

#. If you need to create more than one virtual machine of the same
   configuration, select ``Order multiple Virtual Machines with a similar
   configuration``. See the next section for more details.

#. Click the Accept/Confirm box to confirm confirmation of your purchase.

#. Click ``Order Virtual Machine``.

This action triggers a ticket for your Rackspace VMware Support team
specialist. To track the progress of the ticket, see the ``Track Orders``
section below.

.. warning::

   If the ``Order Virtual Machine`` button is greyed out, this means there's a
   problem with the current selection, for example you may have insufficient
   resources, or there's a compatibility issue. Try selecting another option
   or speak to the Virtualization team for assistance.

Ordering multiple virtual machines
----------------------------------

Use the following steps to order multiple new virtual machines:

#. Select ``Order multiple Virtual Machines with a similar configuration``.

#. Click ``Next Step`` and the ``Multiple Virtual Machines`` page displays.

#. Click ``Add Virtual Machine Copies``.

#. Select either ``Exact Copies`` or ``Modified Copies`` depending on your
   requirements.

#. For ``Exact Copies``:

   #. Enter the quantity.

   #. Click ``Copy Virtual Machine``.

#. For ``Modified Copies``:

   #. Select the ``Root Storage Disk``, ``Root Storage Size``, ``vRAM``, and
      ``Network``.

   #.  Enter the ``Quantity``.

   #. Click ``Copy Virtual Machine``.
