---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-26"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 將服務連接至 Cloud Foundry 應用程式
{: #s2s_binding}

若要在 Cloud Foundry 應用程式中使用服務，您必須建立連線，或將該服務連結至應用程式。
{: shortdesc}

若要從特定服務的詳細資料頁面開始，將服務連接至您的應用程式，請完成下列步驟：

您也可以從應用程式中建立與服務的連線。從資源清單中選取您的應用程式、移至**連線**功能表，然後選取服務。

1. 在資源清單上，按一下**服務**，然後選取您要存取的服務。即會顯示「服務詳細資料」頁面。
2. 按一下導覽中的**連線**。
3. 按一下**建立連線**。
4. 針對您要為其建立連線的應用程式列按一下**連接**。
5. 選取要指派給連線的存取角色。此角色會定義可由存取服務的應用程式執行的可容許動作。
6. 選用項目：選取、建立或自動產生服務 ID，供應用程式用來存取服務。此服務 ID 會獲指派您已在前一個步驟中選取的存取角色。
7. 選用項目：以 JSON 格式新增配置參數。
8. 按一下**連接並重新編譯打包應用程式**。

如果您想要在連接應用程式之後拒絕這些應用程式對服務實例的存取權，請按一下導覽窗格中的**連線**，然後按一下已連接應用程式之功能表中的**取消連結**來移除服務連結。
{: tip}
