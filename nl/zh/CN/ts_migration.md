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

# 有关迁移服务实例的故障诊断

如果在将 Cloud Foundry 服务实例迁移到资源组时遇到任何问题，请查看以下常见问题，以便顺利完成迁移。

## 将服务实例迁移到了错误的资源组中

分配资源后，无法在资源组之间移动这些资源。因此，如果将实例分配给错误的资源组，您可以尝试在目录中删除该实例，然后再创建新实例。在创建实例时，可以将其分配给正确的资源组。

## 帐户中的用户无法迁移有资格迁移的实例

您可能未分配有正确的访问权，因此无法迁移服务实例。有关更多信息，请参阅[谁可以迁移服务实例](/docs/resources/instance_migration.html#whocanmigrate)。

## 不是所有服务都有资格进行迁移

并非所有服务都可通过 Identity and Access Management 添加到资源组并进行管理。如果您有权完成迁移任务，在服务有资格迁移时您会收到相应通知。
