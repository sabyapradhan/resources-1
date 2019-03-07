---

copyright:

  years: 2017, 2019

lastupdated: "2019-02-19"

keywords: migrate, migrating to a resource group, migrate Cloud Foundry

subcollection: resources

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# 將 Cloud Foundry 服務實例及應用程式移轉至資源群組
{: #migrate}

為了讓您有更簡單且更有彈性的 {{site.data.keyword.Bluemix}} 使用體驗，我們推出了[資源群組](/docs/resources?topic=resources-rgs)，其概念類似於 Cloud Foundry 空間。不過，資源群組包含多項額外的好處，例如使用 IBM Cloud Identity and Access Management (IAM) 來進行更精細的存取控制、能夠將服務實例連接至不同地區的應用程式和服務，以及可輕鬆檢視每個群組的用量。
{:shortdesc}

我們已經開始從 Cloud Foundry 移動服務，以利用資源群組的好處，這表示當您在資源清單上看到其中一個服務旁邊的 ![將此服務實例移轉至資源群組](images/migrate.svg "將此服務實例移轉至資源群組") 圖示時，必須為透過 [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://cloud.ibm.com/developer/appservice/dashboard) 建立的服務實例或應用程式開始一個移轉計劃，以從其目前的 Cloud Foundry 組織和空間移至資源群組。在 {{site.data.keyword.Bluemix_notm}} 服務從使用 Cloud Foundry 組織、空間和角色，改為使用 IAM 和資源群組之前，不能將現有的 Cloud Foundry 服務實例移轉至資源群組。

當您將現有的 Cloud Foundry 服務實例或 {{site.data.keyword.dev_console}} 應用程式移轉至資源群組時，移轉完成之後便無法變更您選擇的群組。因此，在移轉之前，請務必規劃好如何組織帳戶中的資源。這可能表示您需要在移轉之前建立一個以上的資源群組，如果您有計費帳戶的話。

您可以嘗試使用與您用 Cloud Foundry 空間來組織資源的相同方式，用資源群組來組織資源。如需使用資源群組的相關資訊，請參閱[用資源群組組織資源的最佳作法](/docs/resources?topic=resources-bp_resourcegroups)。
{: tip}


## 為何要移轉？
{: #why_migrate}

### Cloud Foundry 服務實例
{: #cf_instances}

支援 Cloud IAM 存取控制和資源群組內之組織的服務有幾個優點：

* 您可以利用精細的存取控制，針對個別服務實例或組織成資源群組的一群資源來設定存取權。
* 使用存取群組和資源群組來組織使用者和資源時，只需要設定最少的存取原則數量。例如，您有一組開發人員，您想要讓他們全部都能存取開發環境的資源，則您可以將那些使用者全部組織成一個開發人員存取群組，然後將他們需要存取的所有資源新增至單一資源群組。然後，您可以為存取群組設定單一原則，使其能夠存取資源群組中的所有資源。
* 您可以依資源群組來檢視用量，方法類似於依 Cloud Foundry 組織來檢視用量。
* 您可以連接至任何 Cloud Foundry 空間中的應用程式和服務，這樣可容許從不同地區連接應用程式和服務。當您移轉時，會在您將原始 Cloud Foundry 服務實例轉換為別名，並在您選擇的資源群組中建立鏈結實例時，自動建立連線。下圖顯示使用別名的連線如何運作。

![將服務實例連結至 Cloud Foundry 空間以建立別名](images/alias.svg "將服務實例連結至 Cloud Foundry 空間以建立別名")

### {{site.data.keyword.dev_console}} 應用程式 
{: #app_services}

先前，{{site.data.keyword.dev_console}} 應用程式可能只會與 Cloud Foundry 服務實例相關聯。現在，如果您將應用程式移轉至資源群組，您便可以將應用程式與屬於資源群組且支援 Cloud IAM 存取控制的服務實例相關聯。

## 誰可以移轉？
{: #whocanmigrate}

### 服務實例的必要存取權
{: #required_access_instances}

使用者必須具有特定存取權，才能將 Cloud Foundry 服務實例移轉至資源群組：

* 使用者必須具有 Cloud Foundry 空間的開發人員角色，或實例所屬組織的組織管理員 Cloud Foundry 角色。
* 使用者必須至少具有檢視者 IAM 角色，才能管理實例即將移轉到的目標資源群組。
* 使用者必須至少具有服務的編輯者 IAM 角色。

如需指派正確存取權的相關資訊，請參閱 [Cloud Foundry 存取](/docs/iam?topic=iam-cfaccess)及 [IAM 存取](/docs/iam?topic=iam-userroles#platformrolestable1)。

若要查看您具有哪些存取權，請從主控台功能表列按一下**管理** &gt; **存取 (IAM)**，然後按一下**使用者**。按一下您的名稱，並檢閱已指派 IAM 角色的**存取原則**以及 **Cloud Foundry 存取權**，以查看您有權存取的組織和被指派的 Cloud Foundry 角色。
{: tip}

### {{site.data.keyword.dev_console}} 應用程式的必要存取權
{: #required_access_apps}

可以存取 {{site.data.keyword.dev_console}} 應用程式的任何使用者都可以加以移轉。不過，移轉應用程式並不會移轉與應用程式相關聯的服務。服務實例必須分開移轉。

## 移轉如何運作？
{: #how}

### 移轉服務實例
{: #migrate_instances}

當您將服務實例從 Cloud Foundry 組織及空間移轉至資源群組時，會在資源群組中建立一個新的鏈結服務實例。Cloud Foundry 組織及空間中的原始實例會變成[別名](/docs/resources?topic=resources-connect_app#what_is_alias)。別名會計入您的組織配額，但會針對資源群組中的服務實例用量向您收費。

![將 Cloud Foundry 服務實例移轉至資源群組](images/migration.gif){: gif}

當您在資源清單上收到與 Cloud Foundry 服務實例相關聯的 ![將此服務實例移轉至資源群組](images/migrate.svg "將此服務實例移轉至資源群組") 圖示通知時，會一次移轉一個服務實例。

開始移轉處理程序之前，請檢閱您的服務文件，查看在將服務實例移轉至資源群組時，是否有任何其他必須進行的服務特定變更。例如，如果您刪除 Cloud Foundry 別名，可能會需要將資料從舊實例移轉至新實例，或是更新用於應用程式的認證。如果應用程式直接呼叫所移轉之服務的 API，則需要更新 API 呼叫，以使用 IAM API 金鑰或存取記號。
{: tip}

1. 開啟**更多動作**功能表。
2. 選取**移轉至資源群組**以開始使用。
3. 選取資源群組。
4. 按一下**移轉**，便會為您移轉實例。
5. 由於您一次只能移轉一個實例，所以在移轉第一個實例之後才能繼續移轉符合資格的實例。

順利移轉實例之後，您會在資源清單的「服務」區段中看到它。別名會保留在資源清單的 Cloud Foundry 區段中。您可以使用資源清單 Cloud Foundry 區段中的 ![鏈結圖示](images/link.svg "代表別名的鏈結圖示") 來識別別名。

### 移轉 {{site.data.keyword.dev_console}} 應用程式
{: #migrate_apps}

在「應用程式清單」視圖中，按一下與每個項目相關聯的 ![將此服務實例移轉至資源群組](images/migrate.svg "將此服務實例移轉至資源群組") 圖示，會一次移轉一個應用程式。

1. 選取**功能表**圖示 ![「功能表」圖示](../icons/icon_hamburger.svg)，然後選取有興趣的開發人員入口網站，例如 Watson、行動或 Web 應用程式。
2. 選取**應用程式**，這會顯示**應用程式（需要動作）**及**應用程式（已移轉）**清單。
3. 針對**應用程式（需要動作）**清單中的每個項目，按一下**移轉**圖示 ![將此服務實例移轉至資源群組](images/migrate.svg "將此服務實例移轉至資源群組")。
4. 選取或建立新的資源群組。
5. 按一下**移轉**，便會為您移轉應用程式。
6. 確認應用程式現在顯示於**應用程式（已移轉）**清單。
7. 由於您一次只能移轉一個應用程式，所以在移轉第一個應用程式之後才能繼續移轉符合資格的應用程式。


## 後續步驟
{: #migrate_next_steps}

將 Cloud Foundry 服務實例移轉至資源群組之後，您必須確定帳戶中的使用者擁有必要的存取層次可以存取帳戶資源群組中的資源。您可能也會想要提供用來管理資源群組的存取權，讓使用者可以在帳戶資源群組中建立新的服務實例。

如需指派對資源群組中之資源的存取權相關資訊，請參閱[指派對資源群組及其中資源的存取權](/docs/resources?topic=resources-bp_resourcegroups#assigning_access_rgs)。

此外，也請務必檢閱服務的文件，以查看移轉完成後，是否必須為現有的應用程式進行任何更新。


## 疑難排解
{: #ts_migration}

如果您在移轉 Cloud Foundry 服務實例時遇到任何問題，請參閱[服務及資源的疑難排解](/docs/resources?topic=resources-services)。
