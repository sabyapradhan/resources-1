---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 使用服务端点安全访问服务
{: #service-endpoints}

针对生产工作负载使用基于云的服务的客户需要更多关注安全性。对于许多客户而言，以安全方式访问服务不仅是明智的公司政策，而且在某些情况下，也是遵守法规的要求。{{site.data.keyword.IBM_notm}} 为需要将隔离连接选项用于其工作负载的客户增强了连接选项。 

通过 {{site.data.keyword.cloud}} 服务端点，您可以通过 {{site.data.keyword.cloud_notm}} 专用网络连接到 {{site.data.keyword.cloud_notm}} 服务。从公用网络移走这些工作负载可提供以下两个优点：

* 不再在可通过因特网路由的 IP 地址上提供服务。越来越常见的情况是，云使用者希望限制从其任何服务对公用因特网的访问权或不提供此访问权。现在，使用服务端点功能，服务团队可以针对其服务在专用网络上创建接口，供客户用于进行连接。连接到 {{site.data.keyword.cloud_notm}} 服务不再需要访问因特网。
* 专用网络上没有可计费或计量的带宽费用。过去，在与 {{site.data.keyword.cloud_notm}} 服务进行对话时，会对出口带宽进行计费。 

下图显示在通过服务端点访问云服务时，如何通过 {{site.data.keyword.cloud_notm}} 的专用网络路由流量。

![IBM Cloud 服务端点](images/CSE.png "通过服务端点路由的流量")

要使用 {{site.data.keyword.cloud_notm}} 服务端点，必须在帐户中启用虚拟路由和转发 (VRF)。然后，可以支持使用服务端点。启用这两个选项后，您可以开始创建支持从目录使用 VRF 和服务端点的服务。有关更多信息，请参阅[启用 VRF 和服务端点](/docs/account?topic=account-vrf-service-endpoint)。
