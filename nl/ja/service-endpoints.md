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

# サービス・エンドポイントを使用したサービスへのセキュアなアクセス
{: #service-endpoints}

セキュリティーをさらに重視することが、クラウド・ベース・サービスを実動ワークロードに使用するお客様によって求められています。 多くのお客様にとって、セキュアな方法でサービスにアクセスすることは、賢明な企業戦略というだけではなく、場合によってはコンプライアンス規則を満たすためにも必要です。 {{site.data.keyword.IBM_notm}} は、ワークロードのために隔離接続オプションを必要とするお客様向けに接続オプションを拡張しました。 

{{site.data.keyword.cloud}} サービス・エンドポイントを使用すると、{{site.data.keyword.cloud_notm}} プライベート・ネットワークを介して {{site.data.keyword.cloud_notm}} サービスに接続できます。 これらのワークロードをパブリック・ネットワークから移動することには、次の 2 つの利点があります。

* サービスの処理に、インターネットでルーティング可能な IP アドレスが使用されなくなります。 クラウド・コンシューマーが自身のすべてのサービスからパブリック・インターネットへのアクセスの制限または禁止を望むことがますます一般的になりつつあります。 サービス・チームは、サービス・エンドポイント機能を使用して、サービス用にプライベート・ネットワークを介したインターフェースを作成できるようになりました (顧客はそのインターフェースを使用して接続できます)。 インターネット・アクセスは、{{site.data.keyword.cloud_notm}} サービスに接続するための要件ではなくなりました。
* プライベート・ネットワークには、請求可能な課金も、計量された帯域幅の課金もありません。 これまでは、{{site.data.keyword.cloud_notm}} サービスとの対話時に出口帯域幅について請求されていました。 

以下の図は、サービス・エンドポイントを介してクラウド・サービスにアクセスするときに、{{site.data.keyword.cloud_notm}} のプライベート・ネットワークを介してトラフィックがどのようにルーティングされるのかを示しています。

![IBM Cloud サービス・エンドポイント](images/CSE.png "サービス・エンドポイントを介してルーティングされるトラフィック")

{{site.data.keyword.cloud_notm}} サービス・エンドポイントを使用するには、アカウントで VRF (Virtual Routing and Forwarding) を有効にする必要があります。  その後、サービス・エンドポイントの使用を有効にすることができます。 両方のオプションを有効にした後、カタログから VRF およびサービス・エンドポイントの使用をサポートするサービスの作成を開始できます。 詳しくは、[VRF およびサービス・エンドポイントの有効化](/docs/account?topic=account-vrf-service-endpoint)を参照してください。
