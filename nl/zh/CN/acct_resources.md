---

copyright:

  years: 2018
lastupdated: "2018-05-07"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# 什么是资源？
{: #resource}

资源是可以创建、管理并包含在[资源组](/docs/resources/resourcegroups.html#rgs)中的任何内容。一些示例包括应用程序、服务实例、容器集群、存储卷和虚拟服务器。可在从目录创建时添加到资源组的所有服务实例称为资源，并使用 IAM 访问控制进行管理。支持使用 [IAM 角色进行访问](/docs/iam/users_roles.html#iamusermanrol)并在资源组内进行组织的服务是支持 IAM 的服务。

目前，并非所有服务都支持使用资源组和 IAM。从目录创建时添加到 Cloud Foundry 组织和空间的所有服务实例与支持 IAM 的服务有很大不同。Cloud Foundry 服务与资源组无关，并使用 [Cloud Foundry 角色进行访问权管理](/docs/iam/cfaccess.html#cfaccess)。这些服务称为 Cloud Foundry 服务。服务启用对 IAM 和资源组的支持后，您会收到相关通知，并且会通知您可以使用[将现有 Cloud Foundry 实例迁移到资源组](/docs/resources/instance_migration.html#migrate)。


