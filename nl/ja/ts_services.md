---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-02"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# サービスに関するトラブルシューティング
{: #services}

{{site.data.keyword.Bluemix}} サービスの問題には、ユーザーがサービス・インスタンスを削除した場合に発生するゲートウェイ・タイムアウト・エラーなどが含まれます。 いくつかの簡単なステップに従うことで、これらの問題から復旧できます。
{:shortdesc}

{{site.data.keyword.Bluemix_notm}} 内のサービスにはさまざまなタイプおよび成熟度のレベルがあります。例えば、IBM のサービスとサード・パーティーのサービスがあり、それらのサービスには GA、ベータ、および試験的などの複数のレベルがあります。サービスのタイプおよび成熟度のレベルに基づいて、さまざまなレベルのサポートが提供されている可能性があります。詳細情報については、[サービスのサポートの取得方法 (How do I get support for services?) ](/docs/get-support/servicessupport.html#support-different-services)を参照してください。

## サービス・インスタンスの削除時にサービス・ブローカー・エラーが発生する
{: #ts_service_broker}

クラウド・コントローラーから既に削除されたサービス・インスタンスを削除しようとすると、エラー・メッセージが表示されます。
{:shortdesc}

サービス・インスタンスを削除しようとすると、以下のサービス・ブローカーのエラー・メッセージが表示されます。
{: tsSymptoms}
`ゲートウェイ・タイムアウト (Gateway timeout)`

この問題は、そのサービス・インスタンスが既にクラウド・コントローラーから削除済みである場合に発生します。
{: tsCauses}

同じサービス名でサービス・インスタンスを作成し、それをアプリケーションにバインドします。 その後、そのサービス・インスタンスと、そのサービスを使用するアプリケーションを削除することができます。   
{: tsResolve}
