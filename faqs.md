---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-15"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# FAQs
{: #resources-faq}

## What is a resource group?
{: #resource-group}
{: faq}

A resource group is a way for you to organize your account resources in customizable groupings. Any account resource that is managed by using {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access control belongs to a resource group within your account. You assign resources to a resource group when you create them from the catalog. You can then view usage per resource group in your account, and easily assign users access to all resources in a resource group or just to a single resource in a resource group.

For more information about creating and working with resource groups, see [Managing resource groups](/docs/resources/resourcegroups.html#rgs).  

## Why should I migrate my Cloud Foundry service instances to a resource group?
{: #instance-migrated}
{: faq}

Migrating your Cloud Foundry services to a resource group means that the services you're using are now available for use with IAM access control and resource groups. You can take advantage of fine-grained access control by using IAM roles. You can also view usage per resource group in your account. 

When you have Cloud Foundry services that can be migrated to a resource group, you receive a notification on your resource list. For more information about the migration process, see [Migrating Cloud Foundry service instances and apps to a resource group](/docs/resources/instance_migration.html#migrate).

## Why can’t I create a resource and add it to a resource group?
{: #create-add-resource}
{: faq}

Most likely you're dealing with an access issue. You must have at least the Viewer role on the resource group itself and at least the Editor role on the service in the account. You can contact the account administrator to verify your assigned access in the account. 

## Who can create resource groups?
{: #create-resource}
{: faq}

You can create resource groups only if you're assigned the Administrator role on all {{site.data.keyword.Bluemix_notm}} Identity and Access enabled services in the account.

## Can I delete a resource group?
{: #delete-resource-group}
{: faq}

You can't delete a resource group after it's created.

## Can I move service instances between resource groups?
{: #instances-between-rgs}
{: faq}

You can't move service instances between resource groups. If you assign a service instance incorrectly, you must delete and recreate the instance to assign it to the correct resource group.  

## Can I view usage per resource group?
{: #view-usage}
{: faq}

Yes, you can. To open the Usage Dashboard page, click **Manage** &gt; **Billing and usage**. Select **Usage** to view a summary of the usage by resource group for the account. 
