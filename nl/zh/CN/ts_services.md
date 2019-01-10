---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# 有关服务和资源的故障诊断
{: #services}

服务和资源的一般问题可能包括与删除服务实例相关的问题或与服务迁移相关的问题。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

## 为什么我无法删除服务实例？
{: #ts_service_broker}
{: troubleshoot}

如果尝试删除的服务实例已从云控制器删除，那么可能会收到错误消息。
{:shortdesc}

尝试删除某个服务实例时，显示以下错误消息：
{: tsSymptoms}

`网关超时`

如果该服务实例已从云控制器删除，那么会发生此问题。
{: tsCauses}

您可以使用相同服务名称创建一个服务实例，然后将其绑定到应用程序。这样就可以删除该服务实例以及使用该服务的应用程序了。   
{: tsResolve}

## 为何服务实例会迁移到错误的资源组？ 
{: #ts_service_instance}
{: troubleshoot}

您可能会注意到某个服务实例迁移到了错误的资源组，因此无法重新分配。
{:shortdesc}

分配资源后，无法在资源组之间移动这些资源。
{: tsSymptoms}

您将实例分配给了错误的资源组。  
{: tsCauses}

要更正此问题，您可以尝试在目录中删除该实例，然后再创建新实例。在创建新实例时，可以将其分配给正确的资源组。
{: tsResolve}

## 为什么我不能迁移有资格迁移的实例？
{: #ts_migrate_instance}
{: troubleshoot}

作为帐户中的用户，您在迁移有资格迁移的实例时遇到问题。
{:shortdesc}

您无法迁移有资格迁移的实例。
{: tsSymptoms}

如果您无法迁移有资格迁移的实例，说明您可能没有正确的访问权。
{: tsCauses}

用户必须具有特定访问权才能迁移实例。要查看您拥有的访问权，请在控制台菜单栏中，单击**管理** &gt; **访问权 (IAM)**，然后单击**用户**。单击您的姓名，查看“访问策略”来了解分配的 IAM 角色和 Cloud Foundry 访问权，从而确定您有权访问的组织以及为您分配的 Cloud Foundry 角色。
{: tsResolve}

## 为什么我无法迁移所有服务？
{: #ts_service_migration}
{: troubleshoot}

并非所有服务都有资格迁移。
{:shortdesc}

您无法迁移某些实例。
{: tsSymptoms}

您迁移的服务不可供添加到资源组，并且不是使用 Identity and Access Management (IAM) 进行管理的。如果服务没有资格迁移，那么无法选择迁移。
{: tsCauses}

检查服务以确认它们有资格迁移。您会收到通知并看到 `support_rc_migration` 标志，根据此标志可判断服务是否有资格迁移。
{: tsResolve}
