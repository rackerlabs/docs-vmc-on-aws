:orphan:

=======================
Authentication settings
=======================

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
