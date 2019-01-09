---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# 服務及資源的疑難排解
{: #services}

服務和資源的一般問題可能包括刪除服務實例的問題，或是服務移轉的問題。在許多情況下，您可以遵循一些簡單的步驟，從這些問題回復。
{:shortdesc}

## 為何無法刪除我的服務實例？
{: #ts_service_broker}
{: troubleshoot}

如果嘗試刪除已從雲端控制器刪除的服務實例，您可能會收到錯誤訊息。
{:shortdesc}

嘗試刪除服務實例時，會顯示下列錯誤訊息：
{: tsSymptoms}

`閘道逾時`

如果服務實例已從雲端控制器刪除，則會發生此問題。
{: tsCauses}

請建立具有相同服務名稱的服務實例，然後將它連結至應用程式。然後，您就可以刪除服務實例以及使用該服務的應用程式。   
{: tsResolve}

## 為什麼服務實例會移轉至錯誤的資源群組？ 
{: #ts_service_instance}
{: troubleshoot}

您可能會發現服務實例移轉至錯誤的資源群組，而且無法重新指派。
{:shortdesc}

您在指派資源之後，就無法在資源群組之間移動資源。
{: tsSymptoms}

您已將實例指派給錯誤的資源群組。  
{: tsCauses}

若要更正此問題，您可以嘗試刪除實例，並從型錄建立新的實例。您可以在建立新實例時，將它指派給正確的資源群組。
{: tsResolve}

## 為什麼我無法移轉符合資格的實例？
{: #ts_migrate_instance}
{: troubleshoot}

身為帳戶中的使用者，您在移轉符合資格的實例時發生問題。
{:shortdesc}

您無法移轉符合資格的實例。
{: tsSymptoms}

如果您無法移轉符合資格的實例，表示您可能沒有正確的存取權。
{: tsCauses}

使用者必須具有特定的存取權，才能移轉實例。若要查看您具有哪些存取權，請從主控台功能表列按一下**管理** &gt; **存取 (IAM)**，然後按一下**使用者**。按一下您的名稱並檢閱已指派之 IAM 角色的存取原則和 Cloud Foundry 存取，以查看您有權存取的組織和被指派的 Cloud Foundry 角色。
{: tsResolve}

## 為什麼我無法移轉所有的服務？
{: #ts_service_migration}
{: troubleshoot}

並非所有服務都符合移轉資格。
{:shortdesc}

您無法移轉某些服務。
{: tsSymptoms}

您所移轉的服務無法新增至資源群組，且不是使用 Identity and Access Management (IAM) 進行管理。如果服務不符合資格，就不會有移轉選項。
{: tsCauses}

請檢查服務，以確認其符合移轉資格。您會收到通知，並看到 `support_rc_migration` 旗標，以分辨服務是否符合移轉資格。
{: tsResolve}
