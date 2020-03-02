==================
Enrollment process
==================

The service enrollment process lets you select the virtual machines that
you want to enroll in selected Guest OS Services and provide Rackspace
with OS login credentials that are used to perform the necessary changes,
updates, and additions to the operating system.

VM inventory
~~~~~~~~~~~~

VM creation
-----------

When you create a new VM, an automated system receives a notification from your
vCenter which enables Rackspace to create a CMDB entry in our systems to
represent the new VM. This CMDB entry enables the VM to be displayed in the
list of devices in your account shown in the MyRackspace Portal. Based on the
VM container type, the CMDB device type will indicate that it is Windows,
Linux or Unsupported. The Windows or Linux device types will indicate that it
might qualify for enrollment in Guest OS Services. An Unsupported device type
indicates that the VM container type indicates that the OS of the VM is not
one that Rackspace supports.

For a list of supported OS types and versions, refer to the `EOL Terms
<https://www.rackspace.com/information/legal/eolterms>`_ page. For an OS to be
supported for enrollment in Guest OS Services, the OS type and version must be
listed on the page and must not have reached the "End of Support" date
indicated.

VM device number
----------------

When the VM is registered in the CMDB, it is assigned a device number
identifier.
This number is added to the VM as a custom attribute in vCenter. To see the
device
number for a specific VM, you can search by VM name in the My Rackspace portal
device list, or you can browse to the VM summary tab in vCenter and look at the
custom attribute com.rackspace.deviceId. This CMDB device number is used to
identify the VM when you request Rackspace support services.

.. note::
  If you discover that any of your VMs are missing from the CMDB entries
  displayed in the MyRackspace portal or that they do not have a custom
  attribute
  deviceId value present, contact your account team and provide them with
  the VM name so that an entry can be created.

VM enrollment
~~~~~~~~~~~~~

To enroll a VM or VMs in Guest OS Services, log in to the MyRackspace Portal
with Account Administrator or Device Admin permissions for the VM devices to
be enrolled. To access the enrollment form, a Device Admin user must also have
the Edit Tickets permission because the enrollment form creates a ticket with
the VM devices associated with the ticket.

After logging in to the MyRackspace Portal, select the "Tickets" menu, then
select "Create Tickets". In the "Subject" line, click on the down arrow and
select the "Suggested Templates" item: "Enroll in RPC-VMware Guest OS
Services".

Ticket details
~~~~~~~~~~~~~~

Submitting this form begins the automated process to configure the
selected Guest OS Services for the VMs you specify.
Allow time for the enrollment automation to process your request.
The ticket is updated with comments as your request is processed.

Virtual machines
----------------

Clicking "None selected" displays a list of the VM devices that have been
registered in the Rackspace CMDB based on VM creation events received from you
RPC-VMware vCenter Server. This list only displays VM devices that have not yet
been enrolled in Guest OS Services. Once a device is enrolled, it will be
removed from this list.

From here, you can select the box next to the name of each VM that you want to
enroll in Guest OS Services. You can also use the "Select all" option or the
Search bar to filter for specific VM names.

.. note::
  Only select multiple VMs for enrollment if they share a single user name and
  password as entered below.
  Restrict multiple VM enrollments to no more than 10 VMs.
  Enhancements to the automation process might increase or remove this
  limitation
  in the future.

Managed services
----------------

* [x] OS administration
* [_] Monitoring
* [_] Patching
* [_] Antivirus

Under "Managed Services", you will see a mandatory "OS Administration" service
already selected for you. You can choose to also select the optional
"Monitoring", "Patching" and/or "Antivirus" components. Remember that all VMs
selected will receive the same service selections. If you want to have some
VMs receive different services you will need to enroll them separately.

.. note::
  You must have purchased the corresponding OS service for RPC-VMware in order
  to receive the services selected here. Selecting a service that you have not
  purchased will not result in the service being available for the selected
  VM(s).

Credentials
-----------

Enter the "Username" and "Password" that applies to all selected VMs. The
credentials that you enter here must have Linux root and/or Windows
Administrator level OS permissions.

User account considerations
---------------------------

Windows servers are subject to User Account Control (UAC) by default, which
prevents
remote execution of administrative functions even if the user is an
administrator.

Ensure that UAC is disabled for the account that is used for
enrollment.

.. note::
  Because of UAC, the enrollment account must be a domain account
  and a member of the remote computer Administrators group. If the account is
  a local
  computer member of the Administrators group, then UAC does not allow access
  to the
  WinRM service. To enroll with a local account in a workgroup, UAC filtering
  for
  local accounts must be disabled by creating the following DWORD registry
  entry and
  setting its value to 1:
  ``[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System]
  LocalAccountTokenFilterPolicy``

Rackspace recommends entering Active Directory domain user credentials in the
UPN format
``Username@Domain`` rather than the legacy ``Domain\Username``. This improves
the
reliability of the automated enrollment process.

Linux servers joined to Active Directory allow domain accounts to act as Linux
users.
Due to an issue with open-vm-tools handling of the ``Domain\User`` account
name syntax,
AD users are not currently supported for Linux Guest OS Services enrollment.
Please use
a standard Linux account for the enrollment process.

.. note::
  Because a local account named ``rack`` is created during the enrollment
  process, you cannot use a local account with that name for enrollment
  purposes.

Password limitations
--------------------

Due to the large number of system interactions used for Guest OS Services
automation, only a subset of special characters are supported for user
passwords
submitted for the enrollment process. If you are using special characters in
your
password, include only the following special characters: ``] ! @ # $ % ^ & * (
) { } [``

ASCII code above 127 is not accepted. All other alpha numeric characters are
supported.

Use SSH key
-----------

If you require the use of SSH keys instead of passwords, select the box to
enable SSH Key credentials. After selection, the "Password" field will be
replaced with both "SSH Passphrase" and "SSH Private Key" entry fields.

Submitting the enrollment
-------------------------

Click the "Create Ticket" button to submit the Enrollment request.

Processing the enrollment
-------------------------

Your request will be acknowledged with a ticket that has all of the VM devices
attached for reference. Any issues with the enrollment request will be posted
to the ticket and a final comment will be added when the enrollment process is
complete.

Review all comments in this ticket regarding the individual device
enrollments as well as notes for conditions on some devices that require
action on your part. Closing this ticket indicates your acknowledgement of
these notifications.

Enrollment requirements not met
-------------------------------

Enrollment automation perform checks of the VMs being enrolled to ensure that
they meet the enrollment requirements. If any do not meet the requirements, a
ticket comment is provided to indicate which requirement check failed.
Review the comments carefully and correct any missing requirements before
attempting to enroll the VM again.

Automation failures
-------------------

At times, the automated process encounters failures that require user
intervention.
Support teams are alerted and work to correct any issues as quickly as
possible.
After the issue is resolved, the automation is re-initiated by Rackspace or
manual
enrollment of the requested services is performed.

If errors are noted, do not process any additional enrollments until the error
has been resolved. Also, do not re-submit enrollment requests that are in
progress
as this results in additional tickets for errors that are already being
reviewed and
resolved.

.. note::
  Rackspace does not provide an SLA for the enrollment process. Any SLAs
  related to the
  OS services commences after the service has been configured for the VM.
