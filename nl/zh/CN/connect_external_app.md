---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

---

{: new_window: target="_blank"}
{:shortdesc: .shortdesc}
{: codeblock: .codeblock}
{: tip: .tip}

# 将服务连接到外部应用程序
{: #externalapp}

您可能会有在 {{site.data.keyword.Bluemix}} 外部创建和运行的应用程序，或者您可能会使用第三方工具。如果 {{site.data.keyword.Bluemix_notm}} 服务提供的服务密钥可从因特网访问，那么您可以将这些服务与本地应用程序或第三方工具一起使用。

要允许外部应用程序或第三方工具使用 {{site.data.keyword.Bluemix_notm}} 服务，请完成以下步骤：

大多数服务不需要额外参数；对于需要额外参数的服务，每个服务都会定义自己的唯一参数列表。有关受支持的配置参数的列表，请参阅特定服务产品的文档。
{: tip}

1. 创建服务的实例。
    1. 单击**目录**。
    2. 在“目录”中，通过单击相应服务磁贴来选择所需的服务。 
    3. 选择位置，并选择组织和空间或资源组，然后单击**创建**。
2. 在服务详细信息页面中，选择**服务凭证**来查看或添加 JSON 格式的凭证。 
    * 要创建新凭证，请选择**新建凭证**，还可以选择手动添加配置参数或导入 JSON 格式的文件，然后单击**添加**。选择**查看凭证**以保存用于连接外部应用程序的凭证。
    * 选择一组凭证，然后单击“操作”列中的**查看凭证**（如果已经存在）。 
3. 使用显示的 API 密钥作为凭证来连接到服务实例。

在 {{site.data.keyword.Bluemix_notm}} 外部运行的应用程序现在可以访问 {{site.data.keyword.Bluemix_notm}} 服务。

如果想要删除服务实例或检查计费信息，必须返回到用户界面中用于管理服务实例的“资源列表”。
{: tip}

## 带服务密钥的服务
{: #service_keys}

以下服务会提供服务密钥供您在外部使用：

* {{site.data.keyword.alertnotificationshort}} <!--Alert Notification-->
* {{site.data.keyword.sparks}} <!--Analytics for Apache Spark-->
* {{site.data.keyword.blockchain}} <!--Blockchain-->
* {{site.data.keyword.cloudant}} <!--Cloudant&reg; NoSQL DB-->
* {{site.data.keyword.conversationshort}} <!--Conversation-->
* {{site.data.keyword.discoveryshort}} <!--Discovery-->
* {{site.data.keyword.geospatialshort_Geospatial}} <!--Geospatial Analytics-->
* {{site.data.keyword.GlobalizationPipeline_short}} <!--Globalization Pipeline-->
* {{site.data.keyword.appconserviceshort}} <!--IBM&reg; App Connect-->
* {{site.data.keyword.languagetranslatorshort}} <!--Language Translator-->
* {{site.data.keyword.dwl_short}} <!--Lift-->
* {{site.data.keyword.messagehub}} <!--Message Hub-->
* {{site.data.keyword.nlclassifiershort}} <!--Natural Language Classifier-->
* {{site.data.keyword.objectstorageshort}} <!--Object Storage-->
* {{site.data.keyword.personalityinsightsshort}} <!--Personality Insights-->
* {{site.data.keyword.mobilepush}} <!--Push-->
* {{site.data.keyword.speechtotextshort}} <!-- Speech to Text-->
* {{site.data.keyword.streaminganalyticsshort}} <!--Streaming Analytics-->
* {{site.data.keyword.texttospeechshort}} <!--Text to Speech-->
* {{site.data.keyword.toneanalyzershort}} <!--Tone Analyzer-->
* {{site.data.keyword.weather_short}} <!--Weather Company Data-->
* {{site.data.keyword.workloadscheduler}} <!--Workload Scheduler-->
