---

copyright:

  years: 2017, 2018

lastupdated: "2018-07-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# 将 Cloud Foundry 服务实例和应用程序迁移到资源组
{: #migrate}

为了使您有更简单、更灵活的 {{site.data.keyword.Bluemix}} 使用体验，我们引入了[资源组](/docs/resources/resourcegroups.html#rgs)，资源组在概念上类似于 Cloud Foundry 空间。但是，资源组还包含更多优点，例如使用 IBM Cloud Identity and Access Management (IAM) 进行更细颗粒度的访问控制、能够将服务实例连接到不同区域的应用程序和服务，以及轻松查看每个组的使用情况。
{:shortdesc}

我们要开始将 Cloud Foundry 服务迁移到资源组，以便利用资源组的优点。这意味着，如果在仪表板上看到某个服务的旁边有 ![将此服务实例迁移到资源组](images/migrate.svg " 将此服务实例迁移到资源组") 图标，那么必须为通过 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://console-demo3.bluemix.net/docs/apps/index.html#create) 创建的服务实例或应用程序启动迁移计划，以将其从当前的 Cloud Foundry 组织和空间迁移到资源组。在 {{site.data.keyword.Bluemix_notm}} 服务从使用 Cloud Foundry 组织、空间和角色迁移到使用 IAM 和资源组之后，才能将现有 Cloud Foundry 服务实例迁移到资源组。

如果将现有 Cloud Foundry 服务实例或 {{site.data.keyword.dev_console}} 应用程序迁移到资源组，那么在迁移完成后无法更改所选的资源组。因此，在迁移之前，计划好资源在帐户中的组织方式至关重要。这可能意味着在迁移之前，您需要创建一个或多个资源组（如果您有计费帐户）。 

您可以尝试按照在 Cloud Foundry 空间中组织资源的方式按资源组来组织资源。有关使用资源组的更多信息，请参阅[将资源组织成资源组的最佳实践](/docs/resources/bestpractice_rgs.html#bp_resourcegroups)。
{: tip}


## 为什么要进行迁移？

### Cloud Foundry 服务实例

支持 Cloud IAM 访问控制和在资源组内进行组织的服务有几个优点：

* 通过使用细颗粒度访问控制，可以设置对单个服务实例或对资源组内组织的一组资源的访问权。 
* 通过使用访问组和资源组来组织用户和资源，只需设置最少数量的访问策略。例如，如果您希望一组开发者全部有权访问开发环境的资源，那么可以将所有这些用户组织成开发者访问组，然后将他们需要访问的所有资源添加到一个资源组中。然后，可以为该访问组设置一个策略，使该组有权访问资源组中的所有资源。
* 按资源组查看使用情况时，可以采用与按 Cloud Foundry 组织查看使用情况类似的方式。
* 可以连接到任何 Cloud Foundry 空间中的应用程序和服务。这允许连接不同区域中的应用程序和服务。在进行迁移时，只要将原始 Cloud Foundry 服务实例转变成别名，并在所选资源组中创建链接的实例，连接即会自动完成。下图描绘了使用别名的连接是如何工作的。

![将服务实例绑定到 Cloud Foundry 空间以创建别名](images/alias.svg "将服务实例绑定到 Cloud Foundry 空间以创建别名")

### {{site.data.keyword.dev_console}} 应用程序

以前，{{site.data.keyword.dev_console}} 应用程序只能与 Cloud Foundry 服务实例相关联。现在，如果将应用程序迁移到资源组，那么可以将应用程序与属于资源组并支持 Cloud IAM 访问控制的服务实例相关联。 

## 谁可以进行迁移？
{: #whocanmigrate}

### 服务实例的必要访问权 

用户必须具有特定访问权才能将 Cloud Foundry 服务实例迁移到资源组：

* 用户必须具有对 Cloud Foundry 空间的“开发者”角色，或具有对实例所属组织的“组织管理员”Cloud Foundry 角色。
* 用户必须至少具有“查看者”IAM 角色，才能管理实例要迁移到的资源组。
* 用户必须至少具有对服务的“编辑者”IAM 角色。

有关分配正确访问权的更多信息，请参阅 [Cloud Foundry 访问权](/docs/iam/cfaccess.html#cfaccess)和 [IAM 访问权](/docs/iam/users_roles.html#platformrolestable)。

要查看您拥有的访问权，请在控制台菜单栏中，单击**管理** &gt; **安全性** &gt; **身份和访问权**，然后单击**用户**。单击您的姓名，查看**访问策略**来了解分配给您的 IAM 角色；单击 **Cloud Foundry 访问权**来查看您有权访问的组织以及分配给您的 Cloud Foundry 角色。
{: tip}

### {{site.data.keyword.dev_console}} 应用程序的必要访问权

任何可访问 {{site.data.keyword.dev_console}} 应用程序的用户都可以迁移应用程序。但是，迁移应用程序并不会迁移与应用程序相关联的服务。必须单独迁移服务实例。

## 迁移如何工作？

### 迁移服务实例

将服务实例从 Cloud Foundry 组织和空间迁移到资源组时，会在资源组中新建一个链接的服务实例。Cloud Foundry 组织和空间中的原始实例会变成[别名](/docs/resources/connecting_apps.html#what_is_alias)。别名会计入组织的配额，但计费是基于您在资源组中对服务实例的使用情况。

![将 Cloud Foundry 服务实例迁移到资源组](images/migration.gif){: gif}

当仪表板上显示与 Cloud Foundry 服务实例相关联的 ![将此服务实例迁移到资源组](images/migrate.svg "将此服务实例迁移到资源组") 图标时，就会迁移服务实例（一次一个）。

启动迁移过程之前，请查看服务文档，以了解在将服务实例迁移到资源组时，可能必须进行的其他任何特定于服务的更改。例如，如果删除了 Cloud Foundry 别名，那么可能需要将旧实例中的数据迁移到新实例或更新用于应用程序的凭证。直接调用已迁移服务的 API 的应用程序需要更新该 API 调用，以使用 IAM API 密钥或访问令牌。
{: tip}

1. 打开**更多操作**菜单。
2. 选择**迁移到资源组**以开始迁移。
3. 选择资源组。
4. 单击**迁移**，此时系统会为您迁移实例。
5. 一次只能迁移一个实例，在迁移第一个实例后，您可以继续迁移其他符合要求的实例。

成功迁移实例后，可在仪表板的“服务”部分中看到该实例。别名会保留在仪表板的 Cloud Foundry 部分中。您可以使用仪表板的 Cloud Foundry 部分中的 ![链接图标](images/link.svg "代表别名的链接图标") 来确定别名。

### 迁移 {{site.data.keyword.dev_console}} 应用程序

要迁移应用程序，可以单击“应用程序列表”视图中与每个条目相关联的 ![将此服务迁移到资源组](images/migrate.svg "将此服务迁移到资源组") 图标，一次只能迁移一个应用程序。

1. 选择**菜单**图标 ![菜单图标](../icons/icon_hamburger.svg)，然后选择所需的开发者门户网站，例如 Watson、Mobile 或 Web 应用程序。
2. 选择**应用程序**，此时会显示**应用程序（需要操作）**和**应用程序（已迁移）**列表。
3. 对于**应用程序（需要操作）**列表中的每个条目，单击**迁移**图标 ![将此服务实例迁移到资源组](images/migrate.svg "将此服务实例迁移到资源组")。
4. 选择或创建新的资源组。
5. 单击**迁移**，此时系统会为您迁移应用程序。
6. 确认应用程序现在显示在**应用程序（已迁移）**列表中。
7. 一次只能迁移一个应用程序，因此在迁移完第一个应用程序后，可以继续迁移其他符合要求的应用程序。


## 后续步骤

将 Cloud Foundry 服务实例迁移到资源组后，您需要确保帐户中的用户具有对帐户资源组中资源的必需访问级别。您可能还想提供用于管理资源组的访问权，以便用户可以在帐户资源组中创建新的服务实例。

有关分配对资源组中资源的访问权的更多信息，请参阅[分配对资源组及组内资源的访问权](/docs/resources/bestpractice_rgs.html#assigning-access-to-resource-groups-and-the-resources-within-them)。

此外，请确保查看服务的文档，以了解在迁移完成后是否必须为现有应用程序进行任何更新。 


## 故障诊断

如果在迁移 Cloud Foundry 服务实例时遇到任何问题，请查看[有关迁移服务实例的故障诊断](/docs/resources/ts_migration.html)。
