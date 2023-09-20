---
tags:
  - cloud
  - google
---
# Google Cloud Console
There are four ways to interact with google cloud.
1. Google Cloud console.
2. Cloud SDK and Cloud Shell.
3. APIs
4. Cloud Mobile App
The google cloud console which is google GUI helps deploy, scale and diagnose production issues in a simple web interface.
## Understanding projects
The Google Cloud's hierarchy is made up of four levels, and starting from the bottom up they are:
1. Resources: Is the base layer and represents virtual machines, cloud storage buckets, tables in BigQuery, or anything else in Google Cloud.
2. Projects: Can be organized into folders, or even subfolders.
3. Folders: They are used to organize projects.
4. Organization Node: Has all the projects, folders, and resources that are in current use by the organization.
Each project is a separate compartment, and each resource belongs to exactly one project. Projects can have different owners and users, because they're billed and managed separately.
Each Google Cloud project has three identifying attributes: a project ID, a project name, and a project number. The project ID is a **globally unique** identifier assigned by Google that cannot be changed after creation. The project names, are user-created and can be changed at any time. Google Cloud also assigns each project number, it's helpful to know  that these Google-generated numbers exist and they are mainly used internally by Google to keep track of resources.
## Google Cloud Billing
Billing is stablished at the project level. A billing account can be linked to zero or more projects and they are charged automatically and invoiced every month, or at every threshold limit. Billing sub account can be used to separate billing project.
### Tools help to budget and monitor usage
You’re probably thinking, “How can I make sure I don’t accidentally run up a big Google Cloud bill?”. Google provides a few tools to help:
- Budgets: A budget can be a fixed limit, or it can be tied to another metric such as a percentage of the previous month spend.
- Alerts: It notifies when costs approach your budget limit, you can create an alert. They are generally set at 50%, 90% and 100%, but can be customized.
- Reports: Reports is a visual tool in the Google Cloud console that lets you monitor expenditure based on a project or services.
- Quotas: Google Cloud also implements quotas, which are designed to prevent the over-consumption of resources because of an error or a malicious attack, protecting both account owners and the Google Cloud community as a whole. There are two types of quotas:
	- Rate Quotas: Rate quotas reset after a specific time. For example, by default, the GKE service implements a quota of 1,000 calls to its API from each Google Cloud project every 100 seconds. After that 100 seconds, the limit is reset.
	- Allocation Quotas: Allocation quotas govern the number of resources you can have in your projects. For example, by default, each Google Cloud project has a quota allowing it no more than 5 Virtual Private Cloud networks.