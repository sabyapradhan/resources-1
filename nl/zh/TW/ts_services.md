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


# 服務及資源的疑難排解
{: #services}

{{site.data.keyword.Bluemix}} 服務問題可能包含刪除服務實例的問題。您可以遵循一些簡單的步驟，從這些問題中回復。
{:shortdesc}

## 為何無法刪除我的服務實例？
{: #ts_service_broker}

如果嘗試刪除已從雲端控制器刪除的服務實例，您可能會收到錯誤訊息。
{:shortdesc}

嘗試刪除服務實例時，會顯示下列錯誤訊息：
{: tsSymptoms}

`閘道逾時`

如果服務實例已從雲端控制器刪除，則會發生此問題。
{: tsCauses}

請建立具有相同服務名稱的服務實例，然後將它連結至應用程式。然後，您就可以刪除服務實例以及使用該服務的應用程式。   
{: tsResolve}
