---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 有关服务和资源的故障诊断
{: #services}

{{site.data.keyword.Bluemix}} 服务问题可能包括与删除服务实例相关的问题。只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

## 为什么我无法删除服务实例？
{: #ts_service_broker}

如果尝试删除已从云控制器删除的服务实例，可能会收到错误消息。
{:shortdesc}

尝试删除服务实例时，显示了以下错误消息：
{: tsSymptoms}

`网关超时`

如果已从云控制器删除服务实例，那么会发生此问题。
{: tsCauses}

使用相同服务名称创建服务实例，然后将其绑定到应用程序。随后，可以删除服务实例和使用该服务的应用程序。   
{: tsResolve}
