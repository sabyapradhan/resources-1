---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-20"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 有关服务的故障诊断
{: #services}

{{site.data.keyword.Bluemix}} 服务问题可能包括删除服务实例时发生的网关超时错误。只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

{{site.data.keyword.Bluemix_notm}} 中的服务有不同类型和不同成熟度级别。例如，IBM 服务和第三方服务，以及这些服务的 GA、Beta 和试验等不同级别。根据服务类型和成熟度级别，可能会提供不同级别的支持。有关更多信息，请参阅[如何获得服务支持？](/docs/get-support/servicessupport.html#support-different-services)

## 删除服务实例时服务代理程序发生错误
{: #ts_service_broker}

如果尝试删除已从云控制器删除的服务实例，可能会收到错误消息。
{:shortdesc}

尝试删除服务实例时，看到服务代理程序错误消息：
{: tsSymptoms}
`网关超时`

如果已从云控制器删除服务实例，那么会发生此问题。
{: tsCauses}

使用相同服务名称创建服务实例，然后将其绑定到应用程序。随后，可以删除服务实例和使用该服务的应用程序。   
{: tsResolve}
