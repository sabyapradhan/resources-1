---

copyright:
  years: 2015, 2018
lastupdated: "2018-06-14"

---

{:shortdesc: .shortdesc}

# 在其他区域使用服务
{: #cross_region_service}

如果您在一个区域创建了服务实例并将其绑定到应用程序，那么可以通过以下某种方法，在另外一个区域使用此服务实例：
{: shortdesc}

  * 使用服务凭证来直接配置应用程序实例。有关详细信息，请参阅[允许外部应用程序使用 {{site.data.keyword.Bluemix_notm}} 服务](/docs/apps/reqnsi.html#accser_external){: new_window}。
  * 创建用户提供的服务作为网桥。

	要使用另一个区域中存在的服务实例，请完成以下步骤：

      1. 切换到服务实例所在的区域。在 {{site.data.keyword.Bluemix_notm}} 控制台仪表板中，展开**位置**菜单，然后选择服务实例所在的区域。

      2. 在服务所在的区域中从服务实例的 VCAP_SERVICES 环境变量检索凭证和连接参数。请完成以下步骤：


	       1. 在 {{site.data.keyword.Bluemix_notm}}“仪表板”中，单击应用程序磁贴。这将显示“概述”页面。
	       2. 在导航窗格中，单击**凭证**。这将显示 *VCAP_SERVICES* 环境变量详细信息。记录服务实例的 JSON 内容。

      3. 切换到您要在其中使用服务实例的区域。在 {{site.data.keyword.Bluemix_notm}} 控制台仪表板中，展开**位置**菜单，然后选择要在其中使用服务实例的区域。

      4. 通过使用从 *VCAP_SERVICES* 环境变量记录的凭证和连接参数，以创建用户提供的服务实例。有关信息，请参阅[创建用户提供的服务实例](/docs/apps/reqnsi.html#user_provide_services)。

      5. 通过使用以下命令，将用户创建的服务实例绑定到您的应用程序：

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
