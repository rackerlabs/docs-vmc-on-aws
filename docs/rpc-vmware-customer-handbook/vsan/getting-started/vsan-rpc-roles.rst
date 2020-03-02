
vSAN roles and permissions
--------------------------

To implement the separation of customer and Rackspace duties
in vSAN, Rackspace implements vCenter Server® permissions.

The Customer Access role includes the following privileges to allow
customers to run vSAN health checks and to create vSAN storage
policies.

vSAN health checks
~~~~~~~~~~~~~~~~~~

-  Read access to the cluster
-  Global.Settings
-  Global.Diagnostics
-  Virtual Machine.Create
-  Virtual Machine.Remove

vSAN storage policies
~~~~~~~~~~~~~~~~~~~~~

-  Profile-driven storage.Update
-  Profile-driven storage.View
