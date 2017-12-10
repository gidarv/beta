# Role-Based Access Control and Azure Automation  

Role-Based Access Control (RBAC) allows you to control access to and monitor Microsoft Azure Automation accounts so that you can ensure that resources are not wasted on poorly written automation solutions. You can segregate duties within your team and grant only the amount of access to users, groups, and applications that they need to perform their jobs; for example, if you have an Automation account for East U.S. Automation resources and an Automation account for West U.S. Automation resources, you can separate the administrators of those two resources so that East cannot administer West resources and vice versa. In addition, you might have additional administrators, such as help desk or support personnel, who can monitor an automation object but cannot make any changes.

Each Azure subscription is associated with one Azure Active Directory (AD) directory. Users, groups, and applications from that directory can manage resources in the Azure subscription. Assign these access rights by using the Azure portal, Azure command-line tools, and Azure Management APIs (see diagram).

Grant access by assigning the appropriate RBAC role to users, groups, and applications at a certain scope. The scope of a role assignment can be a subscription, a resource group, or a single resource. A role assigned at a parent scope also grants access to the children contained within it. For example, a user with access to a resource group can manage all the resources it contains, such as websites, virtual machines, and subnets.

![](../../Linked_Image_Files/1.3.2.png)

The RBAC role that you assign dictates what resources the user, group, or application can manage within that scope. Some typical roles include:

1. Owner. An owner can do anything—create objects, delete objects, modify things, and assign permissions to other users.

2. Contributor. A contributor can do everything except modify permissions. A contributor cannot grant someone access to something but can create runbooks, execute them, and run them.

3. Reader. A reader is a view-only administrator; readers can view everything but cannot change anything.

4. Automation operator. An Automation operator can perform tasks that are involved in the operation of an Automation account such as starting and stopping runbooks, but an operator cannot add new runbooks, modify runbooks, modify credentials, or grant permissions.

5. User access administrator. A user access administrator cannot do anything to the Automation objects but can grant and revoke permissions.

For a detailed explanation of specific actions that can be performed by each role, see [RBAC in Automation Accounts](https://docs.microsoft.com/en-us/azure/automation/automation-role-based-access-control#rbac-in-automation-accounts).
