# Create a Project

## From Console

**Go to the Manage resources page in the Cloud Console.**

**GO TO THE MANAGE RESOURCES PAGE**

On the Select organization drop-down list at the top of the page, select the organization in which you want to create a project. 
If you are a free trial user, skip this step, as this list does not appear.

Click Create Project.

In the New Project window that appears, enter a project name and select a billing account as applicable. 
A project name can contain only letters, numbers, single quotes, hyphens, spaces, or exclamation points, and must be between 4 and 30 characters.
Enter the parent organization or folder in the Location box. That resource will be the hierarchical parent of the new project.
When you're finished entering new project details, click Create.


## From gcloud command line

To create a new project, use the gcloud projects create command:

**gcloud projects create PROJECT_ID**

Where PROJECT_ID is the ID for the project you want to create. A project ID must start with a lowercase letter, and can contain only ASCII letters, digits, and hyphens, and must be between 6 and 30 characters.

To create a project with an organization or a folder as parent, use the --organization or --folder flags. As a resource can only have one parent, only one of these flags can be used:

**gcloud projects create PROJECT_ID --organization=ORGANIZATION_ID**

**gcloud projects create PROJECT_ID --folder=FOLDER_ID**


## From Api

You can't use certain words in the project ID when you create a new project with the projects.create() method. Some examples include ssl and google. When you use a restricted word, the request will return with an INVALID_ARGUMENT error.

The below request only creates a project, and does not associate it automatically with a billing account. Use the projects.updateBillingInfo method to set or update the billing account associated with a project.



POST https://cloudresourcemanager.googleapis.com/v1/projects/
Authorization: *************
Content-Type: application/json

{
    "projectId": "our-project-123",
    "name": "my project",
    "labels": {
      "mylabel": "prod"
    }
}
