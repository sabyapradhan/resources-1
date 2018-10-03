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


# サービスとリソースに関するトラブルシューティング
{: #services}

{{site.data.keyword.Bluemix}} サービス問題は、サービス・インスタンスの削除に関する問題を含む場合があります。いくつかの簡単なステップに従うことで、これらの問題から復旧できます。
{:shortdesc}

## なぜサービス・インスタンスを削除できないのですか?
{: #ts_service_broker}

クラウド・コントローラーから既に削除されたサービス・インスタンスを削除しようとすると、エラー・メッセージが表示されることがあります。
{:shortdesc}

サービス・インスタンスを削除しようとすると、以下のエラー・メッセージが表示されます。
{: tsSymptoms}

`ゲートウェイ・タイムアウト (Gateway timeout)`

この問題は、そのサービス・インスタンスが既にクラウド・コントローラーから削除済みである場合に発生します。
{: tsCauses}

同じサービス名でサービス・インスタンスを作成し、それをアプリケーションにバインドします。その後、そのサービス・インスタンスと、そのサービスを使用するアプリケーションを削除することができます。   
{: tsResolve}
