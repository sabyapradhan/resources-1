---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-30"

---

{:shortdesc: .shortdesc}

# 在另一個地區中使用服務
{: #cross_region_service}

如果您的服務實例建立並連結到某個地區中的應用程式，則可以使用下列其中一種方法，在另一個地區中使用這個服務實例：
{: shortdesc}

  * 使用服務認證直接配置應用程式實例。如需詳細資訊，請參閱[將服務連接至外部應用程式](/docs/resources/connect_external_app.html#externalapp)。
  * 建立使用者提供的服務作為橋接器。

	若要使用存在於另一個地區的服務實例，請完成下列步驟：

      1. 若要切換至服務實例所在的地區，請按一下**「功能表」圖示 ![「功能表」圖示](../icons/icon_hamburger.svg)** > **資源清單**。然後，展開**位置**功能表，並選取地區。 

      2. 在服務存在的地區中，從服務實例的 VCAP_SERVICES 環境變數擷取認證及連線參數。請完成下列步驟：

	       1. 在「{{site.data.keyword.Bluemix_notm}} 儀表板」中，按一下應用程式磚上的**檢視全部**。即會顯示「概觀」頁面。
	       2. 在導覽窗格中，按一下**認證**。即會顯示 *VCAP_SERVICES* 環境變數詳細資料。請記錄服務實例的 JSON 內容。

      3. 切換至您要使用服務實例的地區。按一下**「功能表」圖示 ![「功能表」圖示](../icons/icon_hamburger.svg)** > **資源清單**。然後，展開**位置**功能表，並選取您要在其中使用服務實例的地區。

      4. 使用您從 *VCAP_SERVICES* 環境變數記錄的認證及連線參數，建立使用者提供的服務實例。如需相關資訊，請參閱[建立使用者提供的服務實例](/docs/apps/reqnsi.html#user_provide_services)。

      5. 使用下列指令，以將使用者提供的服務實例連結至應用程式：

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
