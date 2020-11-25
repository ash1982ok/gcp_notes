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


### AWS Connector projects
In the preceding diagram, a Google Cloud project connects your monitored AWS account to the Workspace. The AWS connector project can be a Google Cloud project created specifically for this purpose or it can be an existing project. In either case, the AWS connect project must be in the same parent organization as the Workspace. The best practice is to create a Google Cloud project specifically to be the AWS connector project.

In the figure, the connector project has a name beginning with AWS Link. To find the name and details about your AWS connector projects, in the Monitoring menu of the Cloud Console, select Settings.

The billing account associated with the AWS connector project is used for Cloud Monitoring and Cloud Logging charges for the AWS account. For more information, see Billing.

Don't use AWS connector projects for any other purpose, and don't delete them if your Workspace is connected to your AWS account.
