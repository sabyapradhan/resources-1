---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-28"

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

# 設定專用網路端點
{: #private-network-endpoints}

若要透過專用網路連接至 {{site.data.keyword.cloud}} 服務，您必須能夠存取標準基礎架構，並為您的帳戶啟用虛擬遞送及轉遞 (VRF) 和服務端點的連線功能。然後，您可以開始建立服務，以支援專用網路連線的服務端點。
{: shortdesc}

完成下列步驟，以確保已設定您的帳戶，以建立及使用支援服務端點的服務：

1. 確認您是否有權存取帳戶中的 {{site.data.keyword.cloud_notm}} 基礎架構。請移至**功能表**圖示 ![功能表圖示](../icons/icon_hamburger.svg) > **標準基礎架構**，以確認您有存取權。
2. 啟用帳戶的 VRF。如需相關資訊，請參閱[啟用虛擬遞送及轉遞](/docs/account?topic=account-vrf-service-endpoint#vrf)。
3. 啟用帳戶的服務端點連線功能。如需相關資訊，請參閱[啟用服務端點](/docs/account?topic=account-vrf-service-endpoint#vrf)。

啟用 VRF 及服務端點帳戶設定之後，您可以從支援專用網路端點的型錄建立資源。下表列出支援使用專用網路端點的服務。 

如需使用服務端點的相關資訊，請參閱特定服務的文件。
{: tip}

## 支援專用網路端點的服務
{: #services-support-service-endpoints}

|服務| 文件 |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} 服務端點整合](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} 服務端點整合](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} 服務端點整合](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} 服務端點整合](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} 服務端點整合](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [連線功能選項](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [連接至專用端點](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [新增專用端點](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [適用於在 2019 年 1 月 1 日之後部署的所有專用硬體方案](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} 文件](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [管理 {{site.data.keyword.streaminganalyticsshort}} 的服務端點](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [連接至 {{site.data.keyword.cloud_notm}} 專用網路上的 {{site.data.keyword.keymanagementserviceshort}}](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} 文件](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [{{site.data.keyword.containershort_notm}} 的公用及專用服務端點](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) 利用 {{site.data.keyword.keymanagementserviceshort}} 的服務端點進行 BYOK 整合|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} 服務端點整合](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="表 1. 支援使用服務端點的服務" caption-side="top"}










