---

copyright:

  years: 2018

lastupdated: "2018-06-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Troubleshooting migrating service instances

If you run into any issues when you migrate a Cloud Foundry service instance to a resource group, review the following common issues to help you move forward with your migration.

## What if I migrated a service instance into the wrong resource group?

Currently, you can't move resources between resource groups after they are assigned. So, if you migrated an instance into the wrong resource group, you can try deleting the instance and creating a new one from the catalog. You can assign it to the correct resource group when you are creating the instance.

## Why can't I migrate?

You might not be assigned the correct access to migrate a service instance. For more information, see [Who can migrate service instances](/docs/account/instance_migration.html#whocanmigrate).

## Why aren't all services eligible for migration?

Not all services are available to be managed by using IAM access control and resource groups currently. You are notified when services enable the use of IAM, if you have access to complete the migration task.
