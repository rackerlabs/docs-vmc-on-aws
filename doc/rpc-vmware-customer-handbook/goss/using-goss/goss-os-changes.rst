========================
Operating System changes
========================

Enrollment Process OS Changes

When enrolling VMs in Guest OS Services, Rackspace performs the following
steps as part of the enrollment process:

* OS login credentials are validated using VMware tools OS interactions
* OS version is verified using VMware tools OS interactions
* For Windows Servers: WinRM is verified or enabled as needed
* Local IP address is registered with Rackspace systems
* Existing Public IP address from IP allocation device is migrated to VM device
* New Public IP address is provided to VM device if not pre-allocated

After these steps are completed, the automation system makes changes
within the OS of each VM enrolled. You should never adjust
or revert any of these changes when a VM is enrolled in Guest OS Services.
The local OS user account "rack" should never be disabled, renamed, or have the
password changed. Rackspace automatically rotates the password for this
account.

The specific OS service changes are listed below.

Windows OS changes
~~~~~~~~~~~~~~~~~~

OS administration
------------------

* Registry keys to store Rackspace information are created.
* Create a "rack" user account with administrator permission.
* Create a {device#}-admin user account with administrator permission.
* Disable Windows Firewall.

Monitoring
----------

* Download agent installer to c:\\rs-pkgs.
* Install agent and register with the monitoring management system.

Patching
--------

* Configure Rackspace Windows Update Servers.
* Configure Windows Update service settings and restart the service.
* Test the update system access.

Antivirus
----------

* Download agent installer to c:\\rs-pkgs.
* Install agent and register with the antivirus management system.

Linux OS changes
~~~~~~~~~~~~~~~~~

OS administration
-----------------

Create Rackspace user account:

* Create default groups depending on the distribution.
* Create a "rack" user account with root privileges.
* Create a "rack" group.
* Add "rack" to sudoers only in el6.

Create OS associations to Rackspace CMDB entry:

* Create Rackspace cookies and sets the noadc file.
* Cookies are located by default in /root/.rackspace and they are:

    -  customer_number
    -  datacenter
    -  kick
    -  kick_date
    -  segment
    -  server_number
    -  primary_user

* A noadc file is placed in /boot/.rackspace/noadc.

Configure Rackspace time serivce:

* Remove conflicting non-default time service packages (if any).
* Install default time service packages.
* Stop the time service.
* Update the time service configuration files with the Rackspace default
  configuration and time servers (default action, optional).
* Synchronize the server's time.
* Start the time service and enable it to start on boot.

Configure Rackspace DNS:

* Ensure RAX DNSs IPs and search domain are in resolver configuration file.
* Add Rackspace custom NetworkManager config (EL7 only).

Monitoring
----------

* Transfers the installer file.
* Installs and starts the monitoring system agent.
* Removes the installer file.

Patching
--------

* Perform authentication against the RHN API and save the token in
  /tmp/rhnapi_token.
* Verifies whether or not the server is already registered.
* Register the server making these changes.
* Removes the package: subscription-manager.
* Creates a temp directory in the server to download rpm packages that include
  GPG keys.
* Cert packages are installed: rhn-org-trusted-ssl-cert.
* Server is registered using the rhnreg command, using a single registration
  code per device.
* RHN packages are installed: osad, rs-release, rhncfg-actions.
* GPG keys are imported into the rpm db.
* Services are enabled and started: osad, rhnsd.

Ubuntu patching:

* Retrieve a token from the patching system.
* Install python-apt (required by apt_repository).
* Add Rackspace public key.
* Add https Rackspace repository.
* Install rs-inventory.
* Register the VM in inventory.

Antivirus
----------

* Performs connectivity tests to AV system update managers.
* Installs the agent package.
* For Ubuntu 16.04 and RHEL/CentOS 7, switches the on-access detection from
  talpa to fanotify.
