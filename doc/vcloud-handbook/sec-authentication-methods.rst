======================
Authentication methods
======================

VMware vCloud Director uses different authentication mechanisms for
subscriber authentication to the vCloud portal and API.

Internal vCloud accounts
   When configuring a new organization, internal vCloud accounts do not
   use any kind of LDAP service. Instead, new users are configured by
   Rackspace directly in the vCloud User Interface and these users are
   stored within the vCloud database.

   Some of the disadvantages of using internal vCloud authentication
   include:

   -  Groups are unavailable

   -  A minimum length of 6 characters

   -  No password complexity policies

   -  No password expiration policies

   -  No password history

   -  No authentication failure controls

   -  No integration with enterprise identity management systems

vCloud System LDAP Service
   Selecting vCloud System with LDAP Service allows the organization to
   use the Rackspace-provided identity service. Rackspace creates and
   manages users and groups for an organization. Multiple organizations
   can share the same LDAP service.

   .. note::

      This is not a self-service identity solution. Contact Rackspace
      support services for any identity needs.

Custom LDAP Service
   A custom LDAP service enables the organization to use its own
   private LDAP service. Each organization gets a completely separate
   and unique LDAP service. Organizations do not have to use the same
   service as the vCloud system; Dedicated VMware vCloud can use a
   completely separate unique Active Directory forest with no network
   links to any other forest.

   For each organization, a single LDAP service for that organization must be
   configured as a custom LDAP to authenticate to. To enable this
   functionality, the vCloud Director cells must be able to connect to all LDAP
   servers over TCP port 389 or port 636. Network connectivity to each
   organization’s LDAP services **must** be secured. Refer to the `VMware
   vCloud Security Hardening Guide
   <http://www.vmware.com/files/pdf/techpaper/VMW_10Q3_WP_vCloud_Director_Security.pdf>`__
   for more information about the connectivity options for subscriber access to
   LDAP services.

SAML Identity Provider
   A SAML Identity Provider can be used to authenticate users in an
   organization. SAML v2.0 meta data is required for the service to be
   configured. The meta data must include the location of the single
   sign-on service, the single logout service, and the X.509
   certificate for the service.

   When using SAML Identity Providers and API access, follow these
   instructions in the VMware Programming Guide: `Create a Login Session Using
   a SAML Identity Provider
   <https://pubs.vmware.com/vcd-51/index.jsp#com.vmware.vcloud.api.doc_51/GUID-536ED934-ECE3-4B17-B7E5-F8D0765C9ECB.html>`__.

Authentication settings
~~~~~~~~~~~~~~~~~~~~~~~

The following tables show specialized organization settings for email,
LDAP and federation.

.. note::

   Contact Rackspace to request these settings.


**Organization email settings**

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * - Setting
     - Type
     - Description
   * - Use system default SMTP server
     - SMTP Server
     -
   * - Set organization SMTP server
     - SMTP Server
     -
   * - SMTP server name
     - SMTP Server
     - The DNS host name or IP address of the SMTP mail server
   * - SMTP server port
     - SMTP Server
     - The SMTP server port number
   * - Requires Authentication
     - SMTP Server
     - (Optional) Select if the SMTP server requires a user name
   * - User name
     - SMTP Server
     - The user name for the SMTP account
   * - Password
     - SMTP Server
     - The password for the SMTP account
   * - Use system default notification settings
     - Notification Settings
     -
   * - Set organization notification settings
     - Notification Settings
     -
   * - Sender's email address
     - Notification Settings
     - The email address that appears as the sender for vCloud Director emails. vCloud Director uses the sender's email address to send runtime and storage lease expiration alerts.
   * - Email subject prefix
     - Notification Settings
     - The text to use as the subject prefix for vCloud Director emails
   * - Test destination
     - Notification Settings
     - (Optional) Enter a destination email address and click **Test SMTP settings** to test the SMTP settings.


**Organization LDAP settings**

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * - Setting
     - Type
     - Description
   * - Do not use LDAP
     - LDAP Options
     -
   * - VCD system LDAP service
     - LDAP Options
     -
   * - Distinguished name for OU
     - LDAP Options
     -
   * - Custom LDAP service
     - LDAP Options
     - If custom LDAP service is enabled, the following settings are available.
   * - Server
     - Connection
     -
   * - Port
     - Connection
     -
   * - Base distinguished name
     - Connection
     -
   * - SSL
     - Connection
     -
   * - SSL Certificate
     - Connection
     -
   * - Key Store Password
     - Connection
     -
   * - Authentication method
     - Connection
     -
   * - Use external Kerberos
     - Connection
     -
   * - Realm
     - Connection
     -
   * - User name
     - Connection
     -
   * - Password
     - Connection
     -
   * - Enable SSPI
     - SSPI
     -
   * - Service Principal Name
     - SSPI
     -
   * - KeyTab
     - SSPI
     -
   * - Object class
     - User Attributes
     -
   * - Unique identifier
     - User Attributes
     -
   * - User name
     - User Attributes
     -
   * - Display name
     - User Attributes
     -
   * - Given name
     - User Attributes
     -
   * - Surname
     - User Attributes
     -
   * - Email
     - User Attributes
     -
   * - Telephone
     - User Attributes
     -
   * - Group membership identifier
     - User Attributes
     -
   * - Group back link
     - User Attributes
     -
   * - Object class
     - Group Attributes
     -
   * - Unique identifier
     - Group Attributes
     -
   * - Name
     - Group Attributes
     -
   * - Membership
     - Group Attributes
     -
   * - Group membership identifier
     - Group Attributes
     -
   * - Group back link identifier
     - Group Attributes
     -


**Organization federation settings**

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * - Setting
     - Type
     - Description
   * - Use SAML Identity Provider
     - Identity Provider
     -
