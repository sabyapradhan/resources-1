---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

keywords: set up private endpoints, private endpoint, connect service over private network, 

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 设置服务端点
{: #private-network-endpoints}

要通过专用网络连接到 {{site.data.keyword.cloud}} 服务，您必须有权访问经典基础架构，并启用虚拟路由和转发 (VRF) 以及与帐户的服务端点的连接。然后，可以开始创建用于支持专用网络连接的服务端点的服务。
{: shortdesc}

完成以下步骤以确保您的帐户设置为创建和使用支持服务端点的服务：

1. 检查您是否有权在您的帐户中访问 {{site.data.keyword.cloud_notm}} 基础架构。转至**菜单**图标 ![“菜单”图标](../icons/icon_hamburger.svg) > **经典基础架构**以验证您是否具有访问权。
2. 针对 VRF 启用帐户。有关更多信息，请参阅[启用虚拟路由和转发](/docs/account?topic=account-vrf-service-endpoint#vrf)。
3. 针对与服务端点的连接启用帐户。有关更多信息，请参阅[启用服务端点](/docs/account?topic=account-vrf-service-endpoint#service-endpoint)。

启用 VRF 和服务端点帐户设置后，可以从目录创建支持服务端点的资源。下表列出了支持使用服务端点的服务。 

请参阅特定服务的文档以获取有关使用服务端点的更多信息。
{: tip}

## 支持服务端点的服务
{: #services-support-service-endpoints}

|服务|文档|
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} 服务端点集成](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} 服务端点集成](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} 服务端点集成](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} 服务端点集成](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} 服务端点集成](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [连接选项](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [连接到专用端点](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [添加专用端点](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [适用于 2019 年 1 月 1 日后部署的所有专用硬件套餐](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} 文档](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [为 {{site.data.keyword.streaminganalyticsshort}} 管理服务端点](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [在 {{site.data.keyword.cloud_notm}} 专用网络上连接到 {{site.data.keyword.keymanagementserviceshort}}](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} 文档](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [{{site.data.keyword.containershort_notm}} 的公共和专用服务端点](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) 将 {{site.data.keyword.keymanagementserviceshort}} 的服务端点用于其 BYOK 集成|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} 服务端点集成](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="表 1. 支持使用服务端点的服务" caption-side="top"}










