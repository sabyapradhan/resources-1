---

copyright:

  years: 2018
lastupdated: "2018-10-11"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# 什么是资源？
{: #resource}

资源是您可以创建、管理和包含在[资源组](/docs/resources/resourcegroups.html#rgs)中的任何内容。资源的一些示例包括应用程序、服务实例、容器集群、存储卷和虚拟服务器。从目录创建后可添加到资源组的所有服务实例都称为资源，并使用 IAM 访问控制进行管理。支持使用 [IAM 角色进行访问](/docs/iam/users_roles.html#iamusermanrol)和组织成资源组的服务，即为支持 IAM 的服务。

目前，并非所有服务都支持使用资源组和 IAM。从目录创建后添加到 Cloud Foundry 组织和空间的所有服务实例与支持 IAM 的服务有很大不同。Cloud Foundry 服务使用 [Cloud Foundry 角色进行访问权管理](/docs/iam/cfaccess.html#cfroles)，与资源组无关。这些服务称为 Cloud Foundry 服务。服务启用对 IAM 和资源组的支持后，您会收到通知，告知您可以以[将现有 Cloud Foundry 实例迁移到资源组](/docs/resources/instance_migration.html#migrate)。


