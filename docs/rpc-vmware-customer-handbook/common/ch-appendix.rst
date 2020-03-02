:orphan:

========
Appendix
========

Authentication settings
~~~~~~~~~~~~~~~~~~~~~~~

The following tables show organization settings for email, LDAP, and
federation.

Organization email settings
---------------------------

.. list-table::
   :widths: 20 20 60
   :header-rows: 1

   * - **Setting**
     - **Type**
     - **Description**
   * - Use system default SMTP server
     - SMTP server
     -
   * - Set organization SMTP server
     - SMTP server
     -
   * - SMTP server name
     - SMTP server
     - The DNS host name or IP address of the SMTP mail server
   * - SMTP server port
     - SMTP server
     - The SMTP server port number
   * - Requires Authentication
     - SMTP server
     - (Optional) Select if the SMTP server requires a user name
   * - User name
     - SMTP server
     - The user name for the SMTP account
   * - Password
     - SMTP server
     - The password for the SMTP account
   * - Use system default notification settings
     - Notification settings
     -
   * - Set organization notification settings
     - Notification settings
     -
   * - Sender's email address
     - Notification settings
     - The email address that appears as the sender for vCloud
       Director emails. vCloud Director uses the sender's email
       address to send runtime and storage lease expiration alerts.
   * - Email subject prefix
     - Notification settings
     - The text to use as the subject prefix for vCloud Director
       emails emails.
   * - Test destination
     - Notification settings
     - (Optional) Enter a destination email address and click **Test
       SMTP settings** to test the SMTP settings.


Organization LDAP settings
--------------------------

.. list-table::
   :widths: 20 20 60
   :header-rows: 1

   * - **Setting**
     - **Type**
     - **Description**
   * - Do not use LDAP
     - LDAP options
     -
   * - vCloud Director system LDAP service
     - LDAP options
     -
   * - Distinguished name for OU
     - LDAP options
     -
   * - Custom LDAP service
     - LDAP options
     - If custom LDAP service is enabled, the following settings are
       available.
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
   * - SSL certificate
     - Connection
     -
   * - Key store password
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
     - User attributes
     -
   * - Unique identifier
     - User attributes
     -
   * - User name
     - User attributes
     -
   * - Display name
     - User attributes
     -
   * - Given name
     - User attributes
     -
   * - Surname
     - User attributes
     -
   * - Email
     - User attributes
     -
   * - Telephone
     - User attributes
     -
   * - Group membership identifier
     - User attributes
     -
   * - Group back link
     - User attributes
     -
   * - Object class
     - Group attributes
     -
   * - Unique identifier
     - Group attributes
     -
   * - Name
     - Group attributes
     -
   * - Membership
     - Group attributes
     -
   * - Group membership identifier
     - Group attributes
     -
   * - Group back link identifier
     - Group attributes
     -
   * - User name
     - Guest personalization
     -
   * - Password
     - Guest personalization
     -
   * - Account organizational unit
     - Guest personalization
     -


Organization federation settings
--------------------------------

.. list-table::
   :widths: 33 33 33
   :header-rows: 1

   * - **Setting**
     - **Type**
     - **Description**
   * - Use SAML identity provider
     - Identity provider
     -


vCloud permissions
------------------

.. list-table::
   :widths: 12 28 10 10 10 10 10 10
   :header-rows: 1

   * - **Object**
     - **Privileges**
     - **Customer role**
     - Org admin\*
     - Catalog author\*
     - vApp author\*
     - vApp user\*
     - Console only\*
   * - **Catalog**
     - Add vApp from My
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Change owner
     - x
     - x
     -
     -
     -
     -
   * - Catalog
     - VCSP publish subscribe
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Enable a vApp template or media item for download
     - x
     - x
     -
     -
     -
     -
   * - Catalog
     - Create or delete a catalog
     - x
     - x
     - x
     - x
     -
     -
   * - Catalog
     - Edit properties
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Publish
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - Sharing
     - x
     - x
     - x
     -
     -
     -
   * - Catalog
     - View private and shared catalogs
     - x
     - x
     - x
     - x
     -
     -
   * - Catalog
     - View published catalogs
     - x
     - x
     -
     -
     -
     -
   * - Catalog item
     - Create or upload
     - x
     - x
     - x
     -
     -
     -
   * - Catalog item
     - Edit
     - x
     - x
     - x
     -
     -
     -
   * - Catalog item
     - View
     - x
     - x
     - x
     - x
     - x
     -
   * - Catalog item
     - Checkout (add to My Cloud)
     - x
     - x
     - x
     - x
     - x
     -
   * - Catalog item
     - Copy
     - x
     -
     -
     -
     -
     -
   * - Catalog item
     - Enable download
     -
     -
     -
     -
     -
     -
   * - Disk
     - Change owner
     - x
     - x
     - x
     -
     -
     -
   * - Disk
     - Create
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - Delete
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - Edit properties
     - x
     - x
     - x
     - x
     -
     -
   * - Disk
     - View properties
     - x
     - x
     - x
     - x
     -
     -
   * - General
     - Administrator control
     - x
     -
     -
     -
     -
     -
