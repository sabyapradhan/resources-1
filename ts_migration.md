---

copyright:

  years: 2018

lastupdated: "2018-07-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Troubleshooting for migrating service instances

If you run into any issues when you migrate a Cloud Foundry service instance to a resource group, review the following common issues to help you move forward.

## A service instance was migrated to the wrong resource group

You can't move resources between resource groups after they are assigned. So, if you assigned an instance to the wrong resource group, you can try deleting the instance and creating a new one from the catalog. You can assign it to the correct resource group when you create the instance.

## A user in the account can't migrate an eligible instance

You might not be assigned the correct access to migrate a service instance. For more information, see [Who can migrate service instances](/docs/resources/instance_migration.html#whocanmigrate).

## All services aren't eligible for migration

Not all services are available to be added to resource groups and managed by using Identity and Access Management. You are notified when services are eligible, if you have access to complete the migration task.
