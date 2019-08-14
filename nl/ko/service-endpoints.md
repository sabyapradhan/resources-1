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

# 서비스 엔드포인트를 사용하여 서비스에 대한 액세스 보호
{: #service-endpoints}

프로덕션 워크로드에 클라우드 기반 서비스를 사용하는 고객에게는 보안에 대한 높은 관심이 요구됩니다. 많은 고객의 경우 안전한 방식으로 서비스에 액세스하는 것은 현명한 기업 정책일 뿐만 아니라 규제 준수 규정에 필요한 경우도 있습니다. {{site.data.keyword.IBM_notm}}은 워크로드에 대한 격리된 연결 옵션이 필요한 고객을 위해 연결 옵션을 개선했습니다. 

{{site.data.keyword.cloud}} 서비스 엔드포인트를 사용하면 {{site.data.keyword.cloud_notm}} 사설 네트워크를 통해 {{site.data.keyword.cloud_notm}} 서비스에 연결할 수 있습니다. 공용 네트워크에서 이러한 워크로드를 이동하면 다음과 같은 두 가지 장점이 있습니다.

* 서비스는 인터넷 라우팅 가능 IP 주소에서 더 이상 제공되지 않습니다. 클라우드 이용자에게 서비스의 공용 인터넷에 대한 액세스를 제한하거나 액세스하지 못하도록 하는 것이 점점 일반화되고 있습니다. 서비스 엔드포인트 기능을 사용하면 서비스 팀이 고객이 연결에 사용할 수 있는 서비스에 대한 사설 네트워크를 통해 인터페이스를 작성할 수 있습니다. 인터넷 액세스는 더 이상 {{site.data.keyword.cloud_notm}} 서비스에 연결하기 위한 요구사항이 아닙니다.
* 사설 네트워크에 청구 가능하거나 측정된 대역폭 비용이 없습니다. 과거에는 {{site.data.keyword.cloud_notm}} 서비스에 연결할 때 Egress 대역폭에 대한 비용이 청구되었습니다. 

다음 그림은 서비스 엔드포인트를 통해 클라우드 서비스에 액세스할 때 {{site.data.keyword.cloud_notm}}의 사설 네트워크를 통해 트래픽을 라우팅하는 방법을 보여줍니다.

![IBM Cloud 서비스 엔드포인트](images/CSE.png "서비스 엔드포인트를 통해 라우팅되는 트래픽"){: caption="Figure 1. Traffic routed through a service endpoint" caption-side="bottom"}

{{site.data.keyword.cloud_notm}} 서비스 엔드포인트를 사용하려면 계정에서 VRF(Virtual Routing and Forwarding)를 사용으로 설정해야 합니다.  그런 다음 서비스 엔드포인트를 사용으로 설정할 수 있습니다. 두 옵션을 모두 사용으로 설정하면 카탈로그에서 VRF 및 서비스 엔드포인트 사용을 지원하는 서비스 작성을 시작할 수 있습니다. 자세한 정보는 [VRF 및 서비스 엔드포인트 사용](/docs/account?topic=account-vrf-service-endpoint)을 참조하십시오.
