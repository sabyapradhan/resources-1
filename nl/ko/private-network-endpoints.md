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

# 사설 네트워크 엔드포인트 설정
{: #private-network-endpoints}

사설 네트워크를 통해 {{site.data.keyword.cloud}} 서비스에 연결하려면 클래식 인프라에 대한 액세스 권한을 가져야 하며 VRF(Virtual Routing and Forwarding) 및 계정의 서비스 엔드포인트에 대한 연결을 사용으로 설정해야 합니다. 그런 다음 사설 네트워크 연결을 위한 서비스 엔드포인트를 지원하는 서비스 작성을 시작할 수 있습니다.
{: shortdesc}

다음 단계를 완료하여 서비스 엔드포인트를 지원하는 서비스를 작성하고 사용하도록 계정을 설정하십시오.

1. 계정에 {{site.data.keyword.cloud_notm}} 인프라에 대한 액세스 권한이 있는지 확인하십시오. **메뉴** 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg) > **클래식 인프라**로 이동하여 액세스 권한이 있는지 확인하십시오.
2. VRF에 대한 계정을 사용으로 설정하십시오. 자세한 정보는 [VRF(Virtual Routing and Forwarding) 사용](/docs/account?topic=account-vrf-service-endpoint#vrf)을 참조하십시오.
3. 서비스 엔드포인트에 연결하기 위해 계정을 사용으로 설정하십시오. 자세한 정보는 [서비스 엔드포인트 사용](/docs/account?topic=account-vrf-service-endpoint#vrf)을 참조하십시오.

VRF와 서비스 엔드포인트 계정 설정을 사용으로 설정한 후 사설 네트워크 엔드포인트를 지원하는 카탈로그에서 리소스를 작성할 수 있습니다. 다음 표에는 사설 네트워크 엔드포인트 사용을 지원하는 서비스가 나열됩니다. 

서비스 엔드포인트 사용에 대한 자세한 정보는 특정 서비스에 대한 문서를 참조하십시오.
{: tip}

## 사설 네트워크 엔드포인트를 지원하는 서비스
{: #services-support-service-endpoints}

|서비스 |문서 |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} 서비스 엔드포인트 통합](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} 서비스 엔드포인트 통합](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} 서비스 엔드포인트 통합](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} 서비스 엔드포인트 통합](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} 서비스 엔드포인트 통합](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [연결 옵션](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [사설 엔드포인트에 연결](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [사설 엔드포인트 추가](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [2019년 1월 1일 이후 배치된 모든 전용 하드웨어 플랜에 사용 가능](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} 문서](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [{{site.data.keyword.streaminganalyticsshort}}의 서비스 엔드포인트 관리](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [{{site.data.keyword.cloud_notm}} 사설 네트워크의 {{site.data.keyword.keymanagementserviceshort}}에 연결](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} 문서](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [{{site.data.keyword.containershort_notm}}의 공용 및 개인용 서비스 엔드포인트](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints)에서 BYOK 통합을 위한 {{site.data.keyword.keymanagementserviceshort}}의 서비스 엔드포인트 활용|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} 서비스 엔드포인트 통합](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="표 1. 서비스 엔드포인트 사용을 지원하는 서비스" caption-side="top"}










