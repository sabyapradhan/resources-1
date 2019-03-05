---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-07"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# 常見問題 (FAQ)
{: #resources-faq}

## 何謂資源群組？
{: #resource-group}
{: faq}

資源群組可讓您用可自訂的分組來組織帳戶資源。使用 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 存取控制來管理的任何帳戶資源，都屬於您帳戶內的資源群組。當您從型錄建立資源時，會將資源指派給資源群組。然後，您可以檢視帳戶中每個資源群組的用量，並輕鬆地為使用者指派對資源群組中所有資源的存取權，或是只有對資源群組中單一資源的存取權。

如需建立及使用資源群組的相關資訊，請參閱[管理資源群組](/docs/resources?topic=resources-rgs)。  

## 為何我應該將 Cloud Foundry 服務實例移轉至資源群組？
{: #instance-migrated}
{: faq}

將 Cloud Foundry 服務移轉至資源群組，表示您使用中的服務現在已經可以搭配 IAM 存取控制及資源群組來使用。您可以使用 IAM 角色來利用精細的存取控制。也可以檢視帳戶中每個資源群組的用量。

當您有可以移轉至資源群組的 Cloud Foundry 服務時，會在資源清單上收到通知。如需移轉程序的相關資訊，請參閱[將 Cloud Foundry 服務實例及應用程式移轉至資源群組](/docs/resources?topic=resources-migrate)。

## 為何無法建立資源並新增至資源群組？
{: #create-add-resource}
{: faq}

最可能的情況是您在處理存取權問題。您必須至少具有資源群組本身的「檢視者」角色，且至少必須具有帳戶中服務的「編輯者」角色。請在[新增資源至資源群組](/docs/resources?topic=resources-rgs#add_to_rgs)中進一步瞭解。

如需如何檢查已指派存取權的相關資訊，請參閱[檢閱已指派的存取權](/docs/iam?topic=iam-iammanidaccser#review_your_access)。

如果您需要帳戶中的其他存取權，請與[使用者](https://{DomainName}/iam#/users)頁面中所列的帳戶擁有者聯絡。

## 誰可以建立資源群組？
{: #create-resource}
{: faq}

只有在您被指派了帳戶中所有已啟用 {{site.data.keyword.Bluemix_notm}} Identity and Access 之服務的「管理者」角色時，您才能建立資源群組。

## 我可以刪除資源群組嗎？
{: #delete-resource-group}
{: faq}

建立資源群組之後，即無法刪除它。

## 我可以在資源群組之間移動服務實例嗎？
{: #instances-between-rgs}
{: faq}

無法在資源群組之間移動服務實例。如果您錯誤地指派服務實例，則必須刪除並重建該實例，才能將它指派給正確的資源群組。  

## 我可以檢視每個資源群組的用量嗎？
{: #view-usage}
{: faq}

是的，可以。若要開啟「用量儀表板」頁面，請按一下**管理** &gt; **計費及用量**。選取**用量**，即可依帳戶的資源群組來檢視用量摘要。
