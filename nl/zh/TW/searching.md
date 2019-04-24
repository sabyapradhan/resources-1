---

copyright:

  years: 2015, 2019
lastupdated: "2019-02-18"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# 搜尋資源
{: #searching-for-resources}

您可以從 {{site.data.keyword.cloud}} 主控台的任何位置，搜尋您預期在資源清單以及型錄供應項目中找到的已佈建資源。在主控台功能表列的搜尋欄位中，輸入資源或標籤。您也可以使用 {{site.data.keyword.Bluemix_notm}} 指令行介面 (CLI)，在資源之間搜尋。CLI 會跨各個位置和資料中心搜尋分散式應用程式和服務實例。
{:shortdesc}

## 精簡搜尋結果
{: #results}

<dl>
<dt>檢視所有資源結果</dt>
<dd>使用此選項來檢視已過濾的資源清單，該清單會自動移入資源清單中的名稱欄位，為您提供最相關的結果。傳回的搜尋會顯示前 10 個資源結果。如果您知道還有更多結果，可以從資源清單查看所有結果。如果符合資源結果或標籤搜尋，就會出現這個選項。如果不符合資源結果名稱或標籤，則不會出現。</dd>
<dt>檢視所有型錄結果</dt>
<dd>使用此選項來檢視已過濾的型錄搜尋。前五個結果會依名稱顯示。如果您想要使用更詳細的型錄項目搜尋準則（例如搜尋說明內容），可以按一下此鏈結並取得已過濾的型錄結果視圖。此選項可協助您尋找想要更快建立的供應項目。如果符合型錄結果，就會出現這個欄位。如果搜尋查詢的開頭為 `tag:`，則不會出現這個欄位。</dd>
<dt>搜尋支援案例</dt>
<dd>使用此選項可依整個平台中的已開立支援案例進行過濾，包括基礎架構資源。如果您搜尋任何東西（包括依 `tag:` 進行搜尋），這個選項就會出現在搜尋尾端。</dd>
<dt>在文件中搜尋</dt>
<dd>使用此選項以過濾文件。如果您搜尋任何東西（包括依 `tag:` 進行搜尋），這個選項就會出現在搜尋尾端。</dd>
</dl>

按下正斜線鍵 (/)，將游標導覽至搜尋欄位。
{: tip}


## 使用 CLI 進行搜尋
{: #searching-cl}

您也可以使用 Lucene 查詢語法來搜尋您的所有資源（從 0.6.7 版開始，使用 {{site.data.keyword.Bluemix_notm}} CLI 透過單一指令來搜尋）。

  CLI 目前不會搜尋在標準基礎架構實例上執行的資源。
  {: note}

您可以搜尋下列屬性：

<dl>
<dt>`name`</dt>
<dd> 資源的使用者定義名稱。</dd>
<dt>`region`</dt>
<dd>佈建資源的地理位置。容許的值包含 `us-south`、`us-east`、`au-syd`、`eu-gb`、`eu-de` 和 `jp-tok`。</dd>
<dt>`service_name`</dt>
<dd>服務出現在 'ibmcloud catalog service-marketplace' 輸出 Name 直欄中時，所顯示的名稱。</dd>
<dt>`family`</dt>
<dd>資源所屬的雲端元件。容許的值包含 `cloud_foundry`、`containers` 或 `resource_controller`。</dd>
<dt>`organization_id`</dt>
<dd>Cloud Foundry 組織 GUID。</dd>
<dt>`doc.space_id`</dt>
<dd>Cloud Foundry 空間 GUID。</dd>
<dt>`doc.resource_group_id`</dt>
<dd>資源群組的 ID。</dd>
<dt>`type`</dt>
<dd>資源類型。容許的值包含 `k8-cluster`、`cf-service-instance`、`cf-user-provided-service-instance`、`cf-organization`、`cf-service-binding`、`cf-space`、`cf-application`、`resource-instance`、`resource-alias`、`resource-binding` 和 `resource-group`。</dd>
<dt>`creation_date`</dt>
<dd>資源的建立日期。</dd>
<dt>`modification_date`</dt>
<dd> 資源的前次修改日期。</dd>
</dl>

### 搜尋範例
{: #resource-name}

下列範例可協助您搜尋帳戶資源。

* 若要搜尋名稱為 `ABC` 的所有資源，請輸入下列指令。

    `ibmcloud resource search 'name:ABC'`

* 若要搜尋名稱為 `MyResource` 的所有 Cloud Foundry 應用程式，請輸入下列指令。

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* 若要搜尋 Message Hub 的所有服務實例，請輸入下列指令。

    `ibmcloud resource search 'service_name:messagehub'`

* 若要搜尋在 `us-south` 地區之 `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry 組織或 `c900d9671b235c00461c5e311a8aeced` 資源群組中的所有資源，請輸入下列指令。

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* 若要搜尋在 2018 年 5 月 16 至 2018 年 5 月 20 日之間建立的所有資源，請輸入下列指令。

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`

* 若要搜尋名稱開頭為 "my" 且依類型排序的所有資源，請輸入下列指令。

    `ibmcloud resource search 'name:my*' -s type`
