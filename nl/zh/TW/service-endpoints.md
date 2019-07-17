---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-28"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# 專用網路連線的服務端點
{: #service-endpoints}

使用雲端服務來處理正式作業工作負載的客戶需要提高對安全的專注。對許多客戶來說，以安全方式存取服務，並不只是明智的公司原則，在有些情況下也是法規規定所需。對於需要隔離連線功能選項來處理工作負載的客戶，{{site.data.keyword.IBM_notm}} 已加強連線功能選項。 

使用 {{site.data.keyword.cloud}} 服務端點，您可以透過 {{site.data.keyword.cloud_notm}} 專用網路連接至 {{site.data.keyword.cloud_notm}} 服務。從公用網路移動這些工作負載提供兩個優點：

* 在網際網路可遞送的 IP 位址上不再提供服務。雲端消費者越來越常見會想要從他們的任何服務對於公用網際網路只有有限的存取權，或沒有任何存取權。現在，透過服務端點特性，服務團隊可以在專用網路上建立服務的介面，讓客戶可用來連接。網際網路存取不再是您連接至 {{site.data.keyword.cloud_notm}} 服務時的需求。
* 專用網路上沒有可計費或計量的頻寬費用。在過去，與 {{site.data.keyword.cloud_notm}} 服務交談時，會向您收取送出頻寬的費用。 

下圖顯示透過服務端點存取雲端服務時，如何透過 {{site.data.keyword.cloud_notm}} 的專用網路遞送資料流量：

![IBM Cloud 服務端點](images/CSE.png "資料流量透過服務端點遞送"){: caption="圖 1. 資料流量透過服務端點遞送" caption-side="bottom"}

若要使用 {{site.data.keyword.cloud_notm}} 服務端點，您必須在帳戶中啟用虛擬遞送及轉遞 (VRF)。然後，您可以啟用服務端點的使用。啟用這兩個選項之後，您可以開始建立服務，以支援型錄中的 VRF 和服務端點使用。如需相關資訊，請參閱[啟用 VRF 及服務端點](/docs/account?topic=account-vrf-service-endpoint)。
