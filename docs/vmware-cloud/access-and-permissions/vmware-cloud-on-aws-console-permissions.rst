======================================
VMware Cloud on AWS Console permission
======================================

The VMware Cloud on AWS Console is used to manage the VMware Cloud on AWS. The
console is the primary interface for creating SDDCs, adding and removing
hosts, and managing SDDC networking. The console functions are also accessible
by using the API. During the onboarding process, you are asked whether access
to the VMware Cloud on AWS Console is required. You can also request access at
a later time by contacting your Support team. Similarly, you also request
removing user access through a support request.

A registered MyVMware ID is required to receive access to the VMware Cloud on
AWS Console. Rackspace recommends `enabling multifactor authentication <https://docs.vmware.com/en/VMware-Cloud-services/services/Using-VMware-Cloud-Services/GUID-0F036419-1BDE-46D7-A341-7C1D03B367D8.html>`_ on any MyVMware ID
that is granted access to the console.

The following permissions can be granted to the user:

- **Administrator (Delete Restricted)**: The Administrator (Delete Restricted)
  role gets full access to the console except for the **Network and Security**
  tab. This role enables the users to perform operation such as creating SDDCs,
  as well as adding hosts to SDDC clusters. The users cannot remove hosts or
  delete SDDCs.

- **NSX Cloud Admin**: This role provides access to the **Network and
  Security** tab in the VMware Cloud on AWS Console and provides access to
  manage the SDDC network configuration, including VPN connections, firewall
  rules, IP allocation, and NAT configuration. NSX Cloud Admin is granted in
  addition to the Administrator role.
