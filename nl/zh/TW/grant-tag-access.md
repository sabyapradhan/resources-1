---

copyright:

  years: 2018, 2019
lastupdated: "2019-06-03"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# 授與使用者標記資源的存取權
{: #access}

身為帳戶擁有者，您可能會想要委派標記資源的部分責任。若要這麼做，您可以將存取權授與給帳戶中的其他使用者，讓他們能夠新增及移除資源中的標籤。若要讓帳戶中的使用者將標籤新增至資源，必須為他們指派適當的存取權。屬於資源群組之服務的存取權是由 {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) 存取原則進行管理，而屬於 Cloud Foundry 組織和空間之服務的存取權則是由 Cloud Foundry 組織和空間角色進行管理。
{: shortdesc}

## 標記許可權
{: #tagging-permissions}

帳戶中的任何使用者都可以看見標籤。在標記資源之後，對資源具有讀取權的所有使用者都可以看見該標籤。若要新增或移除資源中的標籤，視資源類型而定，會需要特定的存取角色或許可權。請參閱下列表格，以瞭解各資源類型需要什麼角色。


| 資源類型 |角色|
|--------|---------------|
| 已啟用 IAM | 資源的「編輯者」或「管理者」 |
|Cloud Foundry| 資源所屬空間的「開發人員」角色  |
| 標準基礎架構*| 檢視硬體詳細資料許可權或檢視虛擬伺服器詳細資料許可權 |
| 標準基礎架構上的 Cloud Object Storage S3 | 儲存空間管理許可權 |
{: caption="表 1. 新增及移除標籤所需的角色" caption-side="top"}
{: summary="This is a simple data table. However, the asterisk indicates that you must read the qualifying note after this table."}

*標準基礎架構中的可標記資源包含虛擬訪客、虛擬專用主機、網路應用程式遞送控制器、閘道成員、子網路、VLAN 和 VLAN 防火牆（專用）。


## 授與標記已啟用 IAM 之資源的存取權
{: #iam-managed}

屬於資源群組的資源是由 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 存取原則進行管理。請完成下列步驟，將「編輯者」角色指派給使用者，以標記已啟用 IAM 的資源：

  1. 從 {{site.data.keyword.Bluemix_notm}} 主控台按一下**管理 > 存取 (IAM)**，然後選取**使用者**。
  2. 按一下您要授與存取權的使用者名稱。
  3. 按一下**存取原則** > **指派存取權**。
  4. 選取**指派對資源的存取權**選項。
  5. 從服務清單，選取特定的服務或**所有已啟用身分及存取的服務**。
  6. 從平台存取角色清單，選取**編輯者**。
  7. 按一下**指派**。

## 授與標記 Cloud Foundry 資源的存取權
{: #cf_tag_access}

屬於 Cloud Foundry 組織和空間的資源是由 Cloud Foundry 組織和空間角色進行管理。請完成下列步驟，將「開發人員」空間角色指派給使用者，以標記 Cloud Foundry 資源：

 1. 按一下**管理 > 存取 (IAM)**，然後選取**使用者**。
2. 選取您要為其提供存取權的使用者名稱。
3. 按一下 **Cloud Foundry 存取權**。
4. 按一下**指派組織**。
5. 展開並選取具有您要讓使用者存取之服務實例的`組織`。
6. 選取地區。
7. 選取**開發人員**空間角色。
8. 按一下**儲存角色**。

## 授與標記標準基礎架構資源的存取權
{: #classic-infra}

請完成下列步驟，將「管理員」服務存取角色指派給使用者，以標記標準基礎架構服務：

  1. 按一下**管理 > 存取 (IAM)**，然後選取**使用者**。
  2. 按一下您要授與存取權的使用者名稱。
  3. 按一下**標準基礎架構**。
  4. 從**許可權**標籤中，展開**裝置**種類。
  5. 選取**檢視硬體詳細資料**和**檢視虛擬伺服器詳細資料**。如果您需要指派 Cloud Object Storage S3 的存取權，請指派**儲存空間管理**許可權。
  6. 按一下**儲存**。
  7. 按一下**裝置**標籤。
  8. 選取**所有裸機伺服器**或**所有虛擬伺服器**（視您想要標記的資源而定）。
