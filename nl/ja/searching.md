---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-30"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# リソースの検索
{: #searching-for-resources}

{{site.data.keyword.cloud}} コンソール内の任意の場所から、リソース・リストおよびカタログ内のオファリングで検出が必要なプロビジョン済みリソースを検索できます。コンソール・メニュー・バーの検索フィールドにリソースまたはタグを入力します。{{site.data.keyword.Bluemix_notm}} コマンド・ライン・インターフェース (CLI) を使用して、リソース全体で検索することもできます。CLI は、ロケーションおよびデータ・センター全体で分散アプリケーションおよびサービス・インスタンスを検索します。
{:shortdesc}

## 検索結果の絞り込み
{: #results}

<dl>
<dt>すべてのリソース結果の表示</dt>
<dd>このオプションを使用すると、フィルターに掛けられたリソース・リストが表示されます。このリソース・リストの名前フィールドには自動的にデータが取り込まれ、最も関連性の高い結果が得られます。返される検索には、最初の 10 件のリソース結果が表示されます。さらに検索結果がある場合は、それらをすべてリソース・リストから見ることができます。このオプションは、リソース結果またはタグ検索に一致した場合に表示されます。リソースの結果名およびタグと一致しない場合は表示されません。</dd>
<dt>すべてのカタログ結果の表示</dt>
<dd>このオプションを使用して、フィルターに掛けられたカタログ検索を表示します。最初の 5 つの結果が名前で表示されます。説明の検索など、カタログ・エントリーの詳細検索基準が必要な場合は、このリンクをクリックして、フィルターに掛けられたカタログ結果ビューを表示できます。このオプションは、作成するオファリングを迅速に見つけるのに役立ちます。これは、カタログ結果と一致した場合に表示されます。検索照会が `tag:` で始まる場合、このフィールドは表示されません。</dd>
<dt>サポート・ケースでの検索</dt>
<dd>このオプションを使用して、インフラストラクチャー・リソースを含む、プラットフォーム全体のオープン・サポート・ケースでフィルターに掛けます。これは、`tag:` によって検索した場合も含め、何か検索を実行した場合に検索の最後に表示されます。</dd>
<dt>資料内での検索</dt>
<dd>このオプションを使用して、資料をフィルターに掛けて検索します。これは、`tag:` によって検索した場合も含め、何か検索を実行した場合に検索の最後に表示されます。</dd>
</dl>

スラッシュ・キー (/) を押して、カーソルを検索フィールドに移動します。
{: tip}


## CLI を使用した検索
{: #searching-cl}

バージョン 0.6.7 以降、{{site.data.keyword.Bluemix_notm}} CLI で単一のコマンドによって Lucene 照会構文を使用することで、すべてのリソースで検索することもできます。 

  現在、CLI は、従クラシック・インフラストラクチャー・インスタンスで実行されているリソースを検索しません。
  {: note}

以下の属性を検索できます。 

<dl>
<dt>`name`</dt>
<dd> リソースのユーザー定義名。</dd>
<dt>`region`</dt>
<dd>リソースがプロビジョンされている地理的位置。許可される値は、`us-south`、`us-east`、`au-syd`、`eu-gb`、`eu-de`、`jp-tok` です。</dd>
<dt>`service_name`</dt>
<dd>「ibmcloud catalog service-marketplace」の出力の名前列に表示されるサービスの名前。</dd>
<dt>`family`</dt>
<dd>リソースが属するクラウド・コンポーネント。許可される値は、`cloud_foundry`、`containers`、または `resource_controller` です。</dd>
<dt>`organization_id`</dt>
<dd>Cloud Foundry 組織 GUID。</dd>
<dt>`doc.space_id`</dt>
<dd>Cloud Foundry スペース GUID。</dd>
<dt>`doc.resource_group_id`</dt>
<dd>リソース・グループの ID。</dd>
<dt>`type`</dt>
<dd>リソース・タイプ。許可される値は、`k8-cluster`、`cf-service-instance`、`cf-user-provided-service-instance`、`cf-organization`、`cf-service-binding`、`cf-space`、`cf-application`、`resource-instance`、`resource-alias`、`resource-binding`、および `resource-group` です。</dd>
<dt>`creation_date`</dt>
<dd>リソースが作成された日付。</dd>
<dt>`modification_date`</dt>
<dd> リソースの最終変更日。</dd>
</dl>

### 検索の例
{: #resource-name}

以下の例は、アカウント・リソースの検索に役立ちます。

* `ABC` という名前のすべてのリソースを検索するには、以下のコマンドを入力します。

    `ibmcloud resource search ‘name:ABC’`

* `MyResource` という名前のすべての Cloud Foundry アプリケーションを検索するには、以下のコマンドを入力します。

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* メッセージング・ハブのすべてのサービス・インスタンスを検索するには、以下のコマンドを入力します。

    `ibmcloud resource search 'service_name:messagehub'`

* `us-south` 地域の `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry 組織または `c900d9671b235c00461c5e311a8aeced` リソース・グループ内のすべてのリソースを検索するには、以下のコマンドを入力します。

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* 2018 年 5 月 16 日から 2018 年 5 月 20 日までに作成されたすべてのリソースを検索するには、以下のコマンドを入力します。

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* 名前が「my」で始まるすべてのリソースを検索して、タイプで順序付けるには、以下のコマンドを入力します。

    `ibmcloud resource search 'name:my*' -s type`


