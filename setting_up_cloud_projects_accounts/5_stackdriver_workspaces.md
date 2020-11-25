# What is a stackdriver Workspace?

A Workspace is a tool for monitoring resources contained in one or more Google Cloud projects or AWS accounts. 
A Workspace accesses metric data from its monitored projects, but the metric data remains in those projects.

more info - https://cloud.google.com/monitoring/workspaces/

A Google Cloud project or AWS account can be monitored by exactly 1 Workspace. 
A Workspace always monitors its Google Cloud host project. 
However, you can configure a Workspace to monitor up to ***100 Google Cloud*** projects and AWS accounts.

# creating workspaces

https://cloud.google.com/monitoring/workspaces/create

https://cloud.google.com/monitoring/workspaces/create#single-project-workspace

### To create a Workspace, your IAM role name for the Google Cloud project must be one of the following:

Monitoring Editor
Monitoring Admin
Project Owner



### Multi-project Workspace best practice
If you want to create a multi-project Workspace, the best practice is to use the following procedure:

- Create a Google Cloud project to be the Workspace host project. This project should be empty of resources. That is, it doesn't have any VM instances, Cloud Spanner tables, or other resources.

- Create a Workspace for the new project. For details, see Creating a Workspace.

- Add Google Cloud projects or AWS accounts to the Workspace by following the steps in Adding monitored projects.

https://cloud.google.com/monitoring/workspaces/create#first-multi-project-workspace


