======================
Authentication methods
======================

VMware vCloud Director uses different authentication mechanisms for
subscriber authentication to the vCloud Director portal and vCloud API.
Rackspace retains administrator access to vCenter Server and vCloud
Director instances. Customers are given a limited access account.
Elevated access levels are granted only as needed to maintain security.
New users are created on request, except for Active Directory
installations managed by the customer. By default, vCenter Server and
vCloud Director authenticate to the Rackspace Intensive domain.
Rackspace can add your domain to the VMware SSO service for vCenter
Server and the vCloud Director Organization as an additional
authentication source but with the same permission level.

A vCloud Director environment is limited on a per-cell basis to 5000
logged-in users and 1500 active concurrent users. The limit applies to
the total number of users accessing both the vCloud Director portal and
the vCloud API.

If you have multiple Dedicated vClouds at Rackspace, each Dedicated
vCloud environment is self contained, with its own set of user accounts.
Rackspace can provide a single authentication source; for example, the
Intensive domain or Rackspace can create the same local users across all
environments.

For a comprehensive list of authentication settings, please see Appendix
A.

.. note::
   This is not a self-service identity solution. Contact Rackspace support
   services for any identity needs.

Internal accounts
 When configuring a new organization, internal vCloud Director
 accounts do not use any kind of LDAP service. Instead, new users are
 configured by Rackspace directly in the vCloud Director User
 Interface and these users are stored within the vCloud Director
 database.

 Some of the disadvantages of using internal authentication include:

 -  Groups are unavailable
 -  A minimum length of 6 characters
 -  No password complexity policies
 -  No password expiration policies
 -  No password history
 -  No authentication failure controls
 -  No integration with enterprise identity management systems

System LDAP Service
 Selecting the System LDAP Service allows the organization to use the
 Rackspace-provided identity service. Rackspace creates and manages
 users and groups for an organization. Multiple organizations can
 share the same LDAP service.

 .. note::
    This is not a self-service identity solution. Contact Rackspace
    support services for any identity needs.

Custom LDAP Service
 A custom LDAP service enables the organization to use its own
 private LDAP service. Each organization gets a completely separate
 and unique LDAP service. Organizations do not have to use the same
 service as the system level authentication; organizations can use a
 completely separate unique Active Directory forest with no network
 links to any other forest.

 For each organization, a single LDAP service for that organization
 must be configured as a custom LDAP to authenticate to. To enable
 this functionality, the vCloud Director cells must be able to
 connect to all LDAP servers over TCP port 389 or port 636. Network
 connectivity to each organization’s LDAP services **must** be
 secured. Refer to the `VMware vCloud Security Hardening Guide
 <http://www.vmware.com/files/pdf/techpaper/VMW_10Q3_WP_vCloud_Director
 _Security.pdf>`_ for more information about the connectivity options for
 subscriber access to LDAP services.

 .. note::
    vCloud Director does not support hierarchical domains for LDAP
    authentication.

SAML Identity Provider
 A SAML Identity Provider can be used to authenticate users in an
 organization. SAML v2.0 meta data is required for the service to be
 configured. The meta data must include the location of the single
 sign-on service, the single logout service, and the X.509
 certificate for the service.

 When using SAML Identity Providers and API access, follow these
 instructions in the VMware Programming Guide: `Create a Login
 Session Using a SAML Identity Provider <https://pubs.vmware.com/
 vcd-51/index.jsp#com.vmware.vcloud.api.doc_51/GUID-536ED934-ECE3-4B17-B7E5-
 F8D0765C9ECB.html>`_.
