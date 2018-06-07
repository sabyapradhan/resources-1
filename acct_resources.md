---

copyright:

  years: 2018
lastupdated: "2018-05-07"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# What is a resource?
{: #resource}

A resource is anything that can be created, managed, and contained within a [resource group](/docs/resources/resourcegroups.html#rgs). Some examples include apps, service instances, container clusters, storage volumes, and virtual servers. All service instances that can be added to a resource group when they are created from the catalog are called resources and are managed by using IAM access control. The services that support the use of [IAM roles for access](/docs/iam/users_roles.html#iamusermanrol) and organization within a resource group are IAM-enabled services.

Not all services support the use of resource groups and IAM at this time. All service instances that are added to a Cloud Foundry orgs and spaces when they are created from the catalog are distinctly different from IAM-enabled services. Cloud Foundry services have no connection to resource groups and use [Cloud Foundry roles for access management](/docs/iam/cfaccess.html#cfaccess). These services are called Cloud Foundry services. As services enable support for IAM and resource groups, you are notified, you are notified about the ability to [migrate existing Cloud Foundry instances to a resource group](/docs/resources/instance_migration.html#migrate).


