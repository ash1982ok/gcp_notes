# What is a project

The project resource is the base-level organizing entity. Organizations and folders may contain multiple projects.

**All projects consist of the following identifiers:**

- Project ID, which is a unique identifier for the project.

- Project number, which is automatically assigned when you create the project. It is read-only.

- One mutable display name.

- The lifecycle state of the project; for example, ACTIVE or DELETE_REQUESTED.

- A collection of labels that can be used for filtering projects.

- The time when the project was created.

The following code snippet shows the structure of a project:
`
{
  "name": "myproject",
  
  "projectId": "my-project-123",
  
  "labels":
  
   {
   
     "my-label": "prod"
     
   },
   
   "projectNumber": "464036093014",
   
   "lifecycleState": "ACTIVE",
   
   "createTime": "2016-01-07T21:59:43.314Z"
   
}
`

**Project name**: A human-readable name for your project.

The project name isn't used by any Google APIs. You can edit the project name at any time during or after project creation. Project names do not need to be unique.


**Project ID**: A customizable unique identifier for your project.

The project ID is a unique, user-assigned ID that can be used by Google APIs. If you do not specify a project ID during project creation, a project ID will be generated automatically.

The project ID must be a unique string of 6 to 30 lowercase letters, digits, or hyphens. It must start with a letter, and cannot have a trailing hyphen. You cannot change a project ID once it has been created. You cannot re-use a project ID that is in use, or one that has been used for a deleted project.

Some words are restricted from use in project IDs. If you use restricted words in the project name, such as google or ssl, the generated project ID will not include these words.



**Project number**: An automatically generated unique identifier for your project.

