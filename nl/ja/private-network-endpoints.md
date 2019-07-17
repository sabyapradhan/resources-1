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

# プライベート・ネットワーク・エンドポイントのセットアップ
{: #private-network-endpoints}

プライベート・ネットワークを介して {{site.data.keyword.cloud}} サービスに接続するには、クラシック・インフラストラクチャーへのアクセス権限を持っている必要があり、ご使用のアカウントで VRF (Virtual Routing and Forwarding) と、サービス・エンドポイントへの接続を有効にする必要があります。その後、プライベート・ネットワーク接続用のサービス・エンドポイントをサポートするサービスの作成を開始できます。
{: shortdesc}

以下のステップを実行して、サービス・エンドポイントをサポートするサービスを作成および使用するようにアカウントがセットアップされていることを確認します。

1. アカウント内の {{site.data.keyword.cloud_notm}} インフラストラクチャーへのアクセス権限があることを確認します。**メニュー**のアイコン ![メニュー・アイコン](../icons/icon_hamburger.svg) > **「クラシック・インフラストラクチャー」**と進んで、アクセス権限があることを検証します。
2. アカウントで VRF を有効にします。詳しくは、『[Virtual Routing and Forwarding の有効化](/docs/account?topic=account-vrf-service-endpoint#vrf)』を参照してください。
3. アカウントでサービス・エンドポイントへの接続を有効にします。詳しくは、『[サービス・エンドポイントの有効化](/docs/account?topic=account-vrf-service-endpoint#vrf)』を参照してください。

VRF およびサービス・エンドポイントのアカウント設定を有効にした後、プライベート・ネットワーク・エンドポイントをサポートするリソースをカタログから作成できます。プライベート・ネットワーク・エンドポイントの使用をサポートするサービスを次の表に示します。 

サービス・エンドポイントの使用について詳しくは、特定のサービスの資料を参照してください。
{: tip}

## プライベート・ネットワーク・エンドポイントをサポートするサービス
{: #services-support-service-endpoints}

| サービス | 資料 |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} サービス・エンドポイント統合](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} サービス・エンドポイント統合](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} サービス・エンドポイント統合](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} サービス・エンドポイント統合](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} サービス・エンドポイント統合](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [接続オプション](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [プライベート・エンドポイントへの接続](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [プライベート・エンドポイントの追加](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [2019 年 1 月 1 日以降にデプロイされたすべての専用ハードウェア・プランで使用可能](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} 資料](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [{{site.data.keyword.streaminganalyticsshort}} 用のサービス・エンドポイントの管理](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [{{site.data.keyword.cloud_notm}} プライベート・ネットワーク上の {{site.data.keyword.keymanagementserviceshort}} への接続](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} 資料](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [{{site.data.keyword.containershort_notm}} 用のパブリック・サービス・エンドポイントおよびプライベート・サービス・エンドポイント](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) は {{site.data.keyword.keymanagementserviceshort}} のサービス・エンドポイントを BYOK 統合のために使用します|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} サービス・エンドポイント統合](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="表 1. サービス・エンドポイントの使用をサポートするサービス" caption-side="top"}










