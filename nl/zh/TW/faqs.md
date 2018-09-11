---

copyright:

  years: 2015, 2018
  
lastupdated: "2018-08-29"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 常見問題 (FAQ)
{: #resources-faq}

## 何謂資源群組？
{: #resource-group}

資源群組可讓您在可自訂的分組中組織帳戶資源。使用 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 存取控制來管理的任何帳戶資源，都屬於您帳戶內的資源群組。當您從型錄建立資源時，會將資源指派給資源群組。然後，您可以檢視帳戶中每個資源群組的用量，並輕鬆地為使用者指派對資源群組中所有資源的存取權，或是只有對資源群組中單一資源的存取權。

如需建立及使用資源群組的相關資訊，請參閱[管理資源群組](/docs/resources/resourcegroups.html#rgs)。  

## 為何我應該將 Cloud Foundry 服務實例移轉至資源群組？
{: #instance-migrated}

將 Cloud Foundry 服務移轉至資源群組，即表示您使用的服務現在可搭配 IAM 存取控制及資源群組使用。您可以使用 IAM 角色來利用精細的存取控制。您也可以檢視帳戶中每個資源群組的用量。 

當您有可以移轉至資源群組的 Cloud Foundry 服務時，會在儀表板上收到通知。如需移轉程序的相關資訊，請參閱[將 Cloud Foundry 服務實例及應用程式移轉至資源群組](/docs/resources/instance_migration.html#migrate)。

## 為何無法建立資源並新增至資源群組？
{: #create-add-resource}

最可能的情況是您在處理存取問題。您必須至少具有資源群組本身的「檢視者」角色，且至少必須具有帳戶中服務的「編輯者」角色。您可以聯絡帳戶管理者，以驗證您在帳戶中的已指派存取權。 

## 誰可以建立資源群組？
{: #create-resource}

只有您獲得指派對於帳戶中所有具 {{site.data.keyword.Bluemix_notm}} IAM 功能之服務的「管理者」角色時，才能建立資源群組。

## 我可以刪除資源群組嗎？
{: #delete-resource-group}

建立資源群組之後，即無法刪除它。

## 我可以在資源群組之間移動服務實例嗎？
{: #instances-between-rgs}

無法在資源群組之間移動服務實例。如果錯誤地指派服務實例，您必須刪除並重建該實例，才能將它指派給正確的資源群組。  

## 我可以檢視每個資源群組的用量嗎？
{: #view-usage}

是的，可以。若要開啟「用量儀表板」頁面，請按一下**管理 > 計費及用量 > 用量**。您可以檢視該帳戶的資源群組用量摘要。 
