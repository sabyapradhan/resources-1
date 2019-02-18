---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# What is a resource?
{: #resource}

A resource is anything that can be created, managed, and contained within a [resource group](/docs/resources?topic=resources-rgs). Some examples include apps, service instances, container clusters, storage volumes, and virtual servers. All service instances that can be added to a resource group when they're created from the catalog are called resources and are managed by using IAM access control. The services that support the use of [IAM roles for access](/docs/iam?topic=iam-userroles#iamusermanrol) and organization within a resource group are IAM-enabled services.

Not all services support the use of resource groups and IAM currently. All service instances that are added to Cloud Foundry orgs and spaces when they're created from the catalog are distinctly different from IAM-enabled services. Cloud Foundry services have no connection to resource groups and use [Cloud Foundry roles for access management](/docs/iam?topic=iam-cfaccess#cfroles). These services are called Cloud Foundry services. As services enable support for IAM and resource groups, you're notified, you're notified about the ability to [migrate existing Cloud Foundry instances to a resource group](/docs/resources?topic=resources-migrate).


