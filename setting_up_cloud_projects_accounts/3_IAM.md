# IAM (identify and access management)

IAM lets you control who (users) has what access (roles) to which resources by setting IAM policies, 
which grant specific roles that contain certain permissions.

**Permissions**
Permissions allow users to perform specific actions on Google Cloud resources.

**Roles**
You don't directly give users permissions; instead, you grant them roles, which have one or more permissions bundled within them.


NOTE: You grant these roles on a particular resource, but they also apply to all of that resource's descendants in the resource hierarchy.

**Basic Roles**

The following table lists the basic roles that you can grant to access a project, the description of what the role does, and the permissions bundled within that role. 
Avoid using basic roles except when absolutely necessary. 
These roles are very powerful, and include a large number of permissions across all Google Cloud services.

```html
Role	                      Description	                                      Permissions
roles/owner	               Full access to all resources.	                   All permissions for all resources.
roles/editor	              Edit access to all resources.	                    Create and update access for all resources.
roles/viewer	              Read access to all resources.	                    Get and list access for all resources.
roles/browserBeta	         Access to browse resources in the project.	      - resourcemanager.organizations.get
                                                                                - resourcemanager.projects.get
                                                                                - resourcemanager.projects.getIamPolicy
                                                                                - resourcemanager.projects.list
                                                                                - resourcemanager.projectInvites.get
```
Custom Roles that are collections of permissions that you tailor to your needs. 
When creating a Custom Role for use with Resource Manager, be aware of the following points:
 - List and get permissions, such as resourcemanager.projects.get/list, should always be granted as a pair.
 - When your Custom Role includes the folders.list and folders.get permissions, it should also include projects.list and projects.get.
 - Be aware that the setIamPolicy permission for organizations, folders, and projects allows the user to grant all other permissions, and so should be assigned with care.
