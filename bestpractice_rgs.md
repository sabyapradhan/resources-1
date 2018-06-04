---

copyright:

  years: 2018
lastupdated: "2018-05-31"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}


# Best practices for organizing resources in a resource group
{: #bp_resourcegroups}

Resource groups are a feature for organizing your account resources for access control and billing purposes. Access to the resources within a resource group and the resource group itself are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). By using IAM roles, you can provide users access to the resources that are organized within the resource groups. IAM roles can also provide the ability to view, edit, add new service instances to, or manage access to a resource group.

Users are not added to resource groups. Only [resources](/docs/resources/acct_resources.html#resource) can be added. Currently, not all services support the use of IAM access control and the assignment to a resource group. IAM-managed services prompt you to assign new service instances to a resource group when you create them from the catalog. 

You can also find the list of IAM-managed services when you assign access to resources from the Identity and Access UI. Go to **Manage** &gt; **Security** &gt; **Identity and Access**, then select any user or service ID and select **Assign access** from the **Actions** menu. Then, select **Assign access to resources** and in the **Services** drop-down menu you can view the services that support using IAM. For all services that do not yet support using IAM, you can continue to use Cloud Foundry orgs, spaces, and roles. 

Cloud Foundry orgs, spaces, and roles are distinctly separate from resource groups and IAM roles. Therefore, a Cloud Foundry role can never grant access to resources within a resource group. 
{: tip}


## Setting up your resource groups

All users get a single resource group by default that can be renamed. If you have a billable account, you can create more than one resource group for organizing your resources. By organizing resources into different resource groups, you can:

* Make assigning access to a set of resources easier by using a minimal number of policies 
* View by resource group usage information for billing purposes 

If you are familiar with using Cloud Foundry spaces, you can think of organizing resources into resource groups similarly to the way you organized resources into spaces.
{: tip}

To create a new resource group, complete the following steps:

1. Go to **Manage** &gt; **Account** &gt; **Resource Groups**.
2. Click **Create a resource group**.
3. Enter a name for your resource group.
4. Click **Add**.


## Adding resources to a resource group

Services that are managed by using IAM access control belong to a resource group instead of Cloud Foundry org or space. When you create a service instance for one of these services from the catalog, you are prompted to assign the instance to a resource group. 

**Important**: Your resource group selection at the time of creating the instance is final and can't be changed.

You can create a connection between a service instance in a resource group and a Cloud Foundry application. You must have the IAM Editor role on the service instance and the Cloud Foundry developer role on the space the application is in to successfully create the connection. This results in an [alias]((/docs/resources/connecting_apps.html#what_is_alias) for the service instance being created in the Cloud Foundry space where the application is located. Cloud Foundry aliases count toward your account quota.

As more services enable the assignment to resource groups and the use of IAM access control, you are notified on your dashboard if you have existing Cloud Foundry service instances that are eligible for migration. By [migrating a service instance to a resource group](/docs/resources/instance_migration.html), you are creating a new linked instance in a resource group of your choice and the Cloud Foundry instance becomes an alias. 


## Assigning access to resource groups and the resources within them

There are two types of access policies that you need to assign as an account owner to enable the users in your account access to working with resources in resource groups:

* Access to resources within a resource group. Access can be granted to all resources in a group, or only selected services within a group.
* Access to enable the users to manage the group, meaning users can view the group, edit the name of the group, manage access for others to manage the group and most importantly to be able to create and add new service instances to a group.

Review the following table for more information about the two types of access and what each assigned platform IAM role provides a user the ability to do:

| Access policy details  | Actions for access on resource groups | Action on resources in resource groups | 
|:-----------------|:--------------|:---------------|
| Assign access to | Selected resource group | Selected service in a resource group |
| Viewer role  | View the group and its characteristics, but not the resources in the group | View resources in the group | 
| Operator role | Not applicable | Not applicable | 
| Editor role | View or edit name or other characteristics of the group, but not the resources in the group | Create, delete, edit, suspend, resume, view, bind, and manage access of resources in the resource group |
| Administrator role |  View, edit, or manage access for the group, but not the resources in the group | Create, delete, edit, suspend, resume, view, bind, and manage access of resources in the resource group | 
{: caption="Table 1. Access for resource groups" caption-side="top"}

If you want a user to be able to create a new service instance and add it to a resource group, the user must be assigned as a Viewer or above on the resource group and Editor or above on the service.
{: tip}


## Sample access policies

Review the following sample access policies to help you determine how you might want to assign access to resources within your account that belong to resource groups.

1. A policy that grants the user the Platform Role “Administrator” on the {{site.data.keyword.Bluemix_notm}} Container Service across the entire account. A policy with these details allows the user access to all instances of this service and allows the user to create instances of the service in any resource group that the user has at least Viewer role on. Users with the Administrator role on any resource can also grant other users access to that resource.
2. A policy that grants the user the Platform Role “Viewer” on a resource group, but not its member resources. A policy with these details allows the user visibility to the resource group, which is required to create instances of any service in this resource group.
3. A policy that grants the user the Platform Role “Editor” on all resources in the resource group. A user with Editor role on a resource can edit or delete that resource.
4. A policy that grants the user the Platform Role “Administrator” on the entire account (all IAM-enabled services). A policy with these details allows the user to perform any platform actions on any resource in the entire account and also includes the ability to perform management actions on the account such as managing the resource groups in the account.
