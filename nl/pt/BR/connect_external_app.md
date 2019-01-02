---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-07"

---

{: new_window: target="_blank"}
{:shortdesc: .shortdesc}
{: codeblock: .codeblock}
{: tip: .tip}

# Conectando serviços a apps externos
{: #externalapp}

Pode haver aplicativos que foram criados e executados fora
do {{site.data.keyword.Bluemix}}
ou é possível usar ferramentas de terceiros. Se os serviços do {{site.data.keyword.Bluemix_notm}} fornecerem chaves de serviço acessíveis pela internet, será possível usar esses serviços com apps locais ou ferramentas de terceiros.

Para ativar um app externo ou uma ferramenta de terceiro para usar um serviço do {{site.data.keyword.Bluemix_notm}}, conclua as etapas a seguir:

A maioria dos serviços não requer parâmetros extras e, para serviços que fazem isso, cada serviço define sua própria lista exclusiva de parâmetros. Para obter uma lista de parâmetros de configuração suportados, veja a documentação para a oferta de serviços específica.
{: tip}

1. Crie uma instância do serviço.
    1. Clique em **Catálogo**.
    2. No catálogo, selecione o serviço desejado clicando no bloco do serviço. 
    3. Selecione o local, a organização e o espaço ou grupo de recursos e, em seguida, clique em **Criar**.
2. Na página de detalhes do serviço, selecione **Credenciais de serviço** para visualizar ou incluir credenciais no formato JSON. 
    * Para criar novas credenciais, selecione **Nova credencial** e, opcionalmente, inclua parâmetros de configuração manualmente ou importe um arquivo no formato JSON e, em seguida, clique em **Incluir**. Selecione **Visualizar credenciais** para salvar as credenciais para se conectar ao seu app externo.
    * Selecione um conjunto de credenciais e clique em **Visualizar credenciais** na coluna Ações se elas já existirem. 
3. Use a chave de API que é exibida como as credenciais para se conectar à instância de serviço.

Seu aplicativo que é executado fora do {{site.data.keyword.Bluemix_notm}} agora poderá acessar o serviço do {{site.data.keyword.Bluemix_notm}}.

Caso queira excluir instâncias de serviço ou verificar as informações de faturamento, deve-se voltar para a lista Recurso na interface com o usuário para gerenciar as instâncias de serviço.
{: tip}

## Serviços com chaves de serviço

Os serviços a seguir fornecem chaves de serviço para você usar externamente:

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
