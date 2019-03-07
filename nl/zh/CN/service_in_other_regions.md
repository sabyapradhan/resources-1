---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# 在其他区域中使用服务
{: #cross_region_service}

如果您在一个区域中创建了服务实例并将其绑定到应用程序，那么可以使用以下某种方法，在另一个区域中使用此服务实例：
{: shortdesc}

  * 使用服务凭证来直接配置应用程序实例。有关详细信息，请参阅[将服务连接到外部应用程序](/docs/resources?topic=resources-externalapp#externalapp)。
  * 创建一个用户提供的服务来作为桥接服务。

	要使用其他区域中存在的服务实例，请完成以下步骤：

      1. 要切换到服务实例所在的区域，请单击**“菜单”图标 ![“菜单”图标](../icons/icon_hamburger.svg)** > **资源列表**。然后，展开**位置**菜单并选择区域。

      2. 从服务所在区域的服务实例的 VCAP_SERVICES 环境变量中检索凭证和连接参数。请完成以下步骤：


	       1. 在 {{site.data.keyword.Bluemix_notm}}“仪表板”中，单击应用程序磁贴上的**全部查看**。这将显示“概述”页面。
	       2. 在导航窗格中，单击**凭证**。这将显示 *VCAP_SERVICES* 环境变量详细信息。记录服务实例的 JSON 内容。

      3. 切换到您要在其中使用服务实例的区域。单击**“菜单”图标 ![“菜单”图标](../icons/icon_hamburger.svg)** > **资源列表**。接着，展开**位置**菜单，然后选择要在其中使用服务实例的区域。

      4. 通过使用从 *VCAP_SERVICES* 环境变量记录的凭证和连接参数，创建一个用户提供的服务实例。

      5. 使用以下命令，将该用户提供的服务实例绑定到应用程序：

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
