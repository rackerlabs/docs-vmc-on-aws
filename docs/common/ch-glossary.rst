:orphan:

============================
vCloud terms and definitions
============================

Catalogs
    Organizations use catalogs to store vApp templates and media files.
    The members of an organization that have access to a catalog can use
    the catalog's vApp templates and media files to create their own
    vApps. A system administrator can allow an organization to publish a
    catalog to make it available to other organizations. Organizations
    administrators can then choose which catalog items to provide to
    their users.

Cloud Director Networking
    vCloud Director supports three types of networks:

    -  External networks

    -  Organization networks

    -  vApp networks

    Some organization networks and all vApp networks are backed by
    network pools.

Cloud Resources
    Cloud resources are an abstraction of their underlying vSphere
    resources and provide the compute and memory resources for vCloud
    Director virtual machines and vApps, and access to storage and
    network connectivity. A vApp is a virtual system that contains one
    define operational details. Cloud resources include Provider and
    Organization virtual Data Centers, external networks, organization
    networks, and network pools.

External Networks
    An external network is a logical, differentiated network based on a
    vSphere port group. Organization networks can connect to external
    networks to provide Internet connectivity to virtual machines inside
    of a vApp.

Network Pools
    A network pool is a group of undifferentiated networks that is
    available for use within an Org vDC. A network pool is backed by
    vSphere network resources such as VLAN IDs, port groups, or Cloud
    isolated networks. vCloud Director uses network pools to create
    NAT-routed and internal organization networks and all vApp networks.
    Network traffic on each network in a pool is isolated at layer 2
    from all other networks. Each Org vDC in vCloud Director can have
    one network pool. Multiple Org vDCs can share the same network pool.
    The network pool for an organization vDC provides the networks
    created to satisfy the network quota for an Org vDC.

Organizations
    vCloud Director supports multi-tenancy through the use of
    organizations. A vCloud organization is a unit of administration for
    a collection of users, groups, and computing resources. Users
    authenticate at the organization level, supplying credentials
    established by an organization administrator when the user was
    created or imported.

Organization Networks
    An organization network is contained within a vCloud Director
    organization and is available to all the vApps in the organization.
    An organization network allows vApps within an organization to
    communicate with each other. You can connect an organization network
    to an external network to provide external connectivity. Isolated
    organization networks are internal to the organization. Certain
    types of organization networks are backed by network pools.

Organization Virtual Data Centers
    An Organization Virtual Data Center (Org vDC) provides resources to
    an organization and is partitioned from a PvDC. Org vDCs provide an
    environment where virtual systems can be stored, deployed, and
    operated. They also provide storage for virtual media, such as
    floppy disks and CDROMs. A single organization can have multiple Org
    vDCs.

Provider Virtual Data Centers
    A Provider Virtual Data Center (PvDC) combines the compute and
    memory resources of a single vCenter Server resource pool with the
    storage resources of one or more data stores connected to that
    resource pool. Multiple provider vDCs can be created for users in
    different geographic locations or business units, or for users with
    different performance requirements. A PvDC is the source for Org
    vDCs.

Users and Groups
    An organization can contain an arbitrary number of users and groups.
    Users can be created by the organization administrator or imported
    from a directory service such as LDAP. Groups must be imported from
    the directory service. Permissions within an organization are
    controlled through the assignment of rights and roles to users and
    groups.

vApp Network
    A vApp network is contained within a vApp and allows virtual
    machines in the vApp to communicate with each other. A vApp network
    can connect to an organization network to allow the vApp to
    communicate with other vApps in the organization and outside of the
    organization, if the organization network is connected to an
    external network. vApp networks are backed by network pools.

vSphere Resources
    vCloud Director relies on vSphere resources to provide CPU and
    memory to run virtual machines. In addition, vSphere data stores
    provide storage for virtual machine files and other files necessary
    for virtual machine operations. vCloud Director also utilizes
    vNetwork Distributed Switches and vSphere port groups to support
    virtual machine networking. The underlying vSphere resources can be
    used to create cloud resources.
