---

copyright:

  years: 2015, 2018
  
lastupdated: "2018-08-29"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 常见问题
{: #resources-faq}

## 什么是资源组？
{: #resource-group}

资源组是在可定制的分组中组织帐户资源的一种方法。使用 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 访问控制来管理的任何帐户资源都属于您帐户中的资源组。通过目录创建资源时，可向资源组分配这些资源。然后，可以查看帐户中每个资源组的使用情况，并轻松为用户分配对资源组中所有资源的访问权，也可以只分配对资源组中单个资源的访问权。

有关创建和使用资源组的更多信息，请参阅[管理资源组](/docs/resources/resourcegroups.html#rgs)。  

## 为什么应该将 Cloud Foundry 服务实例迁移到资源组？
{: #instance-migrated}

将 Cloud Foundry 服务迁移到资源组意味着您使用的服务现在可供 IAM 访问控制和资源组使用。您可以通过 IAM 角色来利用细颗粒度访问控制。还可以查看帐户中每个资源组的使用情况。 

您具有可迁移到资源组的 Cloud Foundry 服务时，会在仪表板上收到相应通知。有关迁移过程的更多信息，请参阅[将 Cloud Foundry 服务实例和应用程序迁移到资源组](/docs/resources/instance_migration.html#migrate)。

## 为什么无法创建资源并将其添加到资源组？
{: #create-add-resource}

很可能是因为您遇到了访问权问题。您必须至少具有对资源组本身的“查看者”角色，并且至少具有对帐户中服务的“编辑者”角色。您可以联系帐户管理员来验证帐户中分配的访问权。 

## 谁可以创建资源组？
{: #create-resource}

仅当您分配有对帐户中所有启用 {{site.data.keyword.Bluemix_notm}} IAM 的服务的“管理员”角色时，才能创建资源组。

## 可以删除资源组吗？
{: #delete-resource-group}

资源组在创建后无法删除。

## 可以在资源组之间移动服务实例吗？
{: #instances-between-rgs}

不能在资源组之间移动服务实例。如果错误地分配了服务实例，那么必须删除该实例，然后重新创建实例，以将其分配给正确的资源组。  

## 可以查看每个资源组的使用情况吗？
{: #view-usage}

是的，可以。要打开“使用情况仪表板”页面，请单击**管理 > 计费和使用情况 > 使用情况**。您可以按帐户的资源组来查看使用情况摘要。 
