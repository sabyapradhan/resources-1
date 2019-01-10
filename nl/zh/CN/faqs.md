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


# 常见问题
{: #resources-faq}

## 什么是资源组？
{: #resource-group}
{: faq}

资源组是一种使用可定制的分组来组织帐户资源的方法。使用 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 访问控制来管理的任何帐户资源都属于您帐户中的资源组。从“目录”创建资源时，可以将资源分配到资源组中。这样就可以查看帐户中每个资源组的使用情况，还可以轻松地为用户分配对资源组中所有资源的访问权，或只为用户分配对资源组中单个资源的访问权。

有关创建和使用资源组的更多信息，请参阅[管理资源组](/docs/resources/resourcegroups.html#rgs)。  

## 为什么应该将 Cloud Foundry 服务实例迁移到资源组？
{: #instance-migrated}
{: faq}

将 Cloud Foundry 服务迁移到资源组意味着您当前使用的服务现在可与 IAM 访问控制和资源组配合使用。您可以使用 IAM 角色来进行细颗粒度的访问控制。还可以查看帐户中每个资源组的使用情况。 

您具有可迁移到资源组的 Cloud Foundry 服务时，会在资源列表上收到相应通知。有关迁移过程的更多信息，请参阅[将 Cloud Foundry 服务实例和应用程序迁移到资源组](/docs/resources/instance_migration.html#migrate)。

## 为什么无法创建资源并将其添加到资源组？
{: #create-add-resource}
{: faq}

很可能是因为您遇到了访问权问题。您必须至少具有对资源组本身的“查看者”角色，还必须至少具有对帐户中服务的“编辑者”角色。您可以联系帐户管理员来确认帐户中分配给您的访问权。 

## 谁可以创建资源组？
{: #create-resource}
{: faq}

只有为您分配了对帐户中所有启用 {{site.data.keyword.Bluemix_notm}}“身份和访问权”的服务的“管理员”角色时，您才能创建资源组。

## 可以删除资源组吗？
{: #delete-resource-group}
{: faq}

资源组一旦创建便无法删除。

## 可以在资源组之间移动服务实例吗？
{: #instances-between-rgs}
{: faq}

不能在资源组之间移动服务实例。如果错误地分配了服务实例，那么必须删除该实例，然后重新创建实例，以将其分配给正确的资源组。  

## 可以查看每个资源组的使用情况吗？
{: #view-usage}
{: faq}

是的，可以。要打开“使用情况仪表板”页面，请单击**管理** &gt; **计费和使用情况**。选择**使用情况**以按帐户的资源组来查看使用情况摘要。 
