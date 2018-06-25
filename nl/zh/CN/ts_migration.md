---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# 有关迁移服务实例的故障诊断

如果在将 Cloud Foundry 服务实例迁移到资源组时遇到任何问题，请查看以下常见问题，以便顺利完成迁移。

## 如果将服务实例迁移到错误的资源组中该怎么办？

目前，分配资源后，无法在资源组之间移动这些资源。因此，如果将实例迁移到了错误的资源组中，您可以尝试在目录中删除该实例，然后再创建新实例。在创建实例期间，可以将其分配给正确的资源组。

## 为什么我无法执行迁移操作？

您可能没有正确的访问权，因此无法迁移服务实例。有关更多信息，请参阅[谁可以迁移服务实例](/docs/account/instance_migration.html#whocanmigrate)。

## 为什么并非所有服务都符合迁移要求？

目前，并非所有服务都可通过 IAM 访问控制和资源组进行管理。如果您有权完成迁移任务，您会收到服务支持使用 IAM 的通知。
