FAQ
===

**General**

+--------------------------+-------------------------------------------------+
| **Q:** What is Dedicated | **A:** Dedicated VMware vCloud is a private     |
| vCloud?                  | cloud based on VMware services hosted on a      |
|                          | dedicated management cluster. For more          |
|                          | information, see the `Dedicated vCloud product  |
|                          | page <http://www.rackspace.com/managed-virtuali |
|                          | zation/vmware-vcloud>`_.                        |
+--------------------------+-------------------------------------------------+
| **Q:** How do I access   | **A:** Dedicated vCloud environment is only     |
| Dedicated vCloud?        | accessible through a VPN connection to          |
|                          | Rackspace.                                      |
+--------------------------+-------------------------------------------------+
| **Q:** What Rackspace    | **A:** Dedicated vCloud is available in IAD,    |
| data centers provide     | and LON data centers.                           |
| Dedicated vCloud?        |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Are backup and    | **A:** Dedicated vCloud environments are        |
| antivirus included with  | protected using the CommVault SQL server agent  |
| Dedicated vCloud?        | in conjunction with Rackspace VM Recovery,      |
|                          | which is an image-based backup solution.        |
|                          | Antivirus is installed and configured using the |
|                          | latest Rackspace-supported platform. Only VMs   |
|                          | in vApps created from Rackspace catalog         |
|                          | templates with the Managed designation include  |
|                          | backup and antivirus services.                  |
+--------------------------+-------------------------------------------------+
| **Q:** How can I migrate | **A:** Dedicated vCloud provides a way to       |
| virtual machines?        | upload a VM, vApp, or virtual appliance in      |
|                          | either the OVF or OVA format. You can also      |
|                          | migrate data to Rackspace using VMware vCloud   |
|                          | Connector, which is a free tool to move from    |
|                          | your local VMware environment to the            |
|                          | Rackspace-hosted Dedicated vCloud environment.  |
|                          | For additional information about migrating to   |
|                          | Dedicated vCloud, contact Rackspace Support.    |
+--------------------------+-------------------------------------------------+
| **Q:** What versions of  | **A:** Dedicated VMware vCloud supports vCloud  |
| the VMware services are  | Director and vSphere version 5.5 and vROps      |
| currently supported in   | version 6.x.                                    |
| Dedicated VMware vCloud? |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Where can I find  | **A:** Known issues are listed in the release   |
| a list of known issues   | notes for each version of vCloud. You can find  |
| for Dedicated vCloud?    | your version number by clicking **Help** >      |
|                          | **About** in vCloud. For more information, see  |
|                          | the `VMware vCloud Director                     |
|                          | Documentation <https://www.vmware.com/support/p |
|                          | ubs/vcd_pubs.html>`_.                           |
+--------------------------+-------------------------------------------------+

**Access Control**

+--------------------------+-------------------------------------------------+
| **Q:** How are the       | **A:** Rackspace retains administrator access   |
| permissions for users    | to vCenter and vCloud instances. Customers are  |
| controlled in Dedicated  | given a limited access account. Elevated access |
| VMware vCloud?           | levels are granted only as needed to maintain   |
|                          | security. New users are created on request,     |
|                          | except for Active Directory installations       |
|                          | managed by the customer.                        |
+--------------------------+-------------------------------------------------+
| **Q:** How many active   | **A:** A vCloud environment is limited on a per |
| concurrent users can     | cell basis to 5000 logged-in users and 1500     |
| access vCloud?           | active concurrent users. The limit applies to   |
|                          | the total number of users accessing both the    |
|                          | user interface and the API.                     |
+--------------------------+-------------------------------------------------+
| **Q:** Is the same       | **A:** Each vCloud environment is               |
| infrastructure used for  | self-contained, with its own set of user        |
| login information if I   | accounts. Rackspace can provide a single        |
| have multiple vCloud     | authentication source for all environments; for |
| instances in a single    | example, the Intensive domain. Rackspace can    |
| data center?             | create the same local users across all          |
|                          | environments.                                   |
+--------------------------+-------------------------------------------------+
| **Q:** What single sign  | **A:** By default, vCenter and vCloud           |
| on (SSO) capabilities    | authenticate to the Rackspace Intensive domain. |
| are provided?            | Rackspace can add your domain to the VMware SSO |
|                          | service for vCenter and the vCloud Organization |
|                          | as an additional authentication source.         |
+--------------------------+-------------------------------------------------+
| **Q:** What are the      | **A:** Customer role limitations are described  |
| restrictions to vCloud   | in the features and permissions tables in our   |
| features?                | `Dedicated vCloud                               |
|                          | Handbook <https://docs.rackspace.com/vcloud     |
|                          | /api/v1/bk-dedicated-%20vcloud-handbook/content |
|                          | /vclo ud-common-front.html>`_.                  |
+--------------------------+-------------------------------------------------+

**Architecture**

+--------------------------+-------------------------------------------------+
| **Q:** Are Dedicated     | **A:** Yes, Dedicated vCloud environments are   |
| vCloud environments      | deployed in HA configuration.                   |
| deployed in high         |                                                 |
| availability (HA)        |                                                 |
| configuration?           |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Is there a limit  | **A:** Rackspace does not impose a limit on VMs |
| to the number of VMs per | per environment. We can provide recommendations |
| environment?             | for best practices to maintain optimal          |
|                          | performance.                                    |
+--------------------------+-------------------------------------------------+
| **Q:** Can I access the  | **A:** Yes. You can access vCloud and vSphere   |
| vCenter API? Can I       | APIs, subject to permissions restrictions on a  |
| access the vCloud API?   | user account.                                   |
+--------------------------+-------------------------------------------------+
| **Q:** Can I do a        | **A:** No, stretching the data link layer       |
| stretched layer 2 to     | across environments is not supported in         |
| allow vMotion between my | Dedicated vCloud.                               |
| existing sites?          |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Can I add ESXi    | **A:** No. Only hypervisors provided by         |
| hypervisors in my data   | Rackspace can be added.                         |
| center to the Dedicated  |                                                 |
| VMware vCloud            |                                                 |
| environment?             |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Can I manage      | **A:** We do not provide direct access to the   |
| Rackspace-hosted VMware  | hypervisor. You can make hypervisor change      |
| ESXi hypervisors if I    | requests by creating a Rackspace support        |
| have Dedicated VMware    | ticket.                                         |
| vCloud?                  |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** With Dedicated    | **A:** Import and export privileges are not     |
| VMware vCloud, do I have | provided on individual hypervisors. You can     |
| full control over ESXi   | upload images to your Dedicated vCloud          |
| hypervisors to import or | environment using the OVF Import function of    |
| export my own VMs?       | vCloud Connector.                               |
+--------------------------+-------------------------------------------------+
| **Q:** Can I manage      | **A:** No, write access to the vCenter server   |
| vCenter plugins and add  | is not provided.                                |
| my own third party       |                                                 |
| plugins?                 |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Are Storage RDMs  | **A:** Yes, by opening a support ticket with    |
| supported?               | our storage and virtualization team.            |
+--------------------------+-------------------------------------------------+

**Integration**

+--------------------------+-------------------------------------------------+
| **Q:** What other VMware | **A:** Dedicated vCloud allows customers to use |
| products are supported?  | other VMware products like vRealize Automation, |
|                          | but these products are not fully supported by   |
|                          | Rackspace.                                      |
+--------------------------+-------------------------------------------------+
| **Q:** Is Rackspace      | **A:** Yes.                                     |
| RackConnect supported    |                                                 |
| with Dedicated VMware    |                                                 |
| vCloud?                  |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Does the MyRack   | **A:** Yes, you can view devices on MyRack.     |
| portal work with vCloud? |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** You can view      | **A:** You can deploy vCloud Connector, but     |
| devices in the MyRack    | Rackspace does not provide support for it.      |
| portal, but VM           |                                                 |
| management is only       |                                                 |
| available when using the |                                                 |
| vCloud portal or API.    |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** Can I deploy      | **A:** Yes.                                     |
| AlertLogic IDS with      |                                                 |
| Dedicated VMware vCloud? |                                                 |
+--------------------------+-------------------------------------------------+

**Monitoring**

+--------------------------+-------------------------------------------------+
| **Q:** How are the       | **A:** The management infrastructure is         |
| components of this       | monitored using a combination of tools.         |
| product monitored?       |                                                 |
|                          |     -  **HP SiteScope for vCenter services**.   |
|                          |        This alerts Rackspace virtualization     |
|                          |        engineers when any web services          |
|                          |        associated with Dedicated vCloud and     |
|                          |        vCloud Director are unavailable.         |
|                          |     -  **Rackwatch for hypervisor               |
|                          |        connectivity**. This alerts Rackspace    |
|                          |        virtualization engineers when devices    |
|                          |        don't respond to ping requests.          |
|                          |     -  **CA Nimsoft Monitor for vCenter         |
|                          |        alarms**. This alerts Rackspace          |
|                          |        virtualization engineers to alarms       |
|                          |        raised in vCenter.                       |
|                          |                                                 |
|                          | Any supported vApps deployed from the           |
|                          | Rackspace-provided catalog are monitored by     |
|                          | these systems.                                  |
+--------------------------+-------------------------------------------------+
| **Q:** Is monitoring     | **A:** No.                                      |
| available for my         |                                                 |
| unsupported VMs?         |                                                 |
+--------------------------+-------------------------------------------------+
| **Q:** How do I know if  | **A:** Dedicated vCloud includes vRealize       |
| resources are low?       | Operations (vROps) if the customer purchases    |
|                          | Rackspace-provided ESXi licensing. vROps        |
|                          | provides advanced reporting and forecasting     |
|                          | capabilities, as well as the ability to set     |
|                          | Smart Alerts to notify you when resources are   |
|                          | low. This IT operations management tool can be  |
|                          | helpful when optimizing resources and           |
|                          | identifying performance bottlenecks.            |
+--------------------------+-------------------------------------------------+
