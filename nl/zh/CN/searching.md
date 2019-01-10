---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-30"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# 搜索资源
{: #searching-for-resources}

您可以在 {{site.data.keyword.cloud}} 控制台中的任何位置搜索应该在资源列表中找到的已供应资源，也可以在目录中搜索产品。请在控制台菜单栏的搜索字段中输入资源或标记。您还可以使用 {{site.data.keyword.Bluemix_notm}} 命令行界面 (CLI) 在各资源中进行搜索。CLI 会在各个位置和数据中心内搜索分布式应用程序和服务实例。
{:shortdesc}

## 优化搜索结果
{: #results}

<dl>
<dt>查看所有资源结果</dt>
<dd>使用此选项可查看自动填充资源列表中名称字段的已过滤资源列表，从而为您提供最相关的结果。返回的搜索将显示前 10 个资源结果。如果您知道还有更多结果，那么可以在资源列表中查看所有这些结果。如果与资源结果或标记搜索相匹配，那么会显示此选项。如果与资源结果名称或标记不匹配，那么不会显示此选项。</dd>
<dt>查看所有目录结果</dt>
<dd>使用此选项可查看过滤的目录搜索。这将按名称显示前 5 个结果。如果要对目录条目应用更详细的搜索条件（例如，搜索描述），那么可以单击此链接来获取过滤的目录结果视图。此选项可帮助您更快找到要创建的产品。如果与目录结果相匹配，那么会显示此选项。如果搜索查询以 `tag:` 开头，那么不会显示此字段。</dd>
<dt>搜索支持案例</dt>
<dd>使用此选项可按平台中打开的支持案例（包括基础架构资源）进行过滤。如果搜索任何内容（包括按 `tag:` 进行搜索），那么会在搜索结束时显示此选项。</dd>
<dt>在文档中搜索</dt>
<dd>使用此选项可获取文档的过滤视图。如果搜索任何内容（包括按 `tag:` 进行搜索），那么会在搜索结束时显示此选项。</dd>
</dl>

按“正斜杠”键 (/) 可将光标移动到搜索字段。
{: tip}


## 使用 CLI 进行搜索
{: #searching-cl}

您还可以在 {{site.data.keyword.Bluemix_notm}} CLI（从 V0.6.7 开始）中，使用 Lucene 查询语法通过一个命令在所有资源中进行搜索。 

  CLI 目前不会搜索在经典基础架构实例上运行的资源。
  {: note}

可以搜索以下属性： 

<dl>
<dt>`name`</dt><dd> 用户定义的资源名称。</dd>
<dt>`region`</dt>
<dd>供应资源的地理位置。允许的值为 `us-south`、`us-east`、`au-syd`、`eu-gb`、`eu-de` 和 `jp-tok`。</dd>
<dt>`service_name`</dt>
<dd>在“ibmcloud catalog service-marketplace”的输出的 Name 列中显示的服务名称。</dd>
<dt>`family`</dt>
<dd>资源所属的云组件。允许的值为 `cloud_foundry`、`containers` 或 `resource_controller`。</dd>
<dt>`organization_id`</dt>
<dd>Cloud Foundry 组织 GUID。</dd>
<dt>`doc.space_id`</dt>
<dd>Cloud Foundry 空间 GUID。</dd>
<dt>`doc.resource_group_id`</dt>
<dd>资源组的标识。</dd>
<dt>`type`</dt>
<dd>资源类型。允许的值为 `k8-cluster`、`cf-service-instance`、`cf-user-provided-service-instance`、`cf-organization`、`cf-service-binding`, `cf-space`、`cf-application`、`resource-instance`、`resource-alias`、`resource-binding` 和 `resource-group`。</dd>
<dt>`creation_date`</dt>
<dd>创建资源的日期。</dd>
<dt>`modification_date`</dt>
<dd> 上次修改资源的日期。</dd>
</dl>

### 搜索示例
{: #resource-name}

以下示例可帮助您搜索帐户资源。

* 要搜索名为 `ABC` 的所有资源，请输入以下命令。

    `ibmcloud resource search ‘name:ABC’`

* 要搜索名为 `MyResource` 的所有 Cloud Foundry 应用程序，请输入以下命令。

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* 要搜索 Message Hub 的所有服务实例，请输入以下命令。

    `ibmcloud resource search 'service_name:messagehub'`

* 要搜索 `us-south` 区域中 `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry 组织中或 `c900d9671b235c00461c5e311a8aeced` 资源组中的所有资源，请输入以下命令。

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* 要搜索在 2018 年 5 月 16 日至 2018 年 5 月 20 日之间创建的所有资源，请输入以下命令。

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* 要搜索名称以“my”开头的所有资源且按类型排序，请输入以下命令。

    `ibmcloud resource search 'name:my*' -s type`


