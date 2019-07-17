---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-28"

keywords: set up private endpoints, private endpoint, connect service over private network, 

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Configurando terminais de rede privada
{: #private-network-endpoints}

Para se conectar aos serviços {{site.data.keyword.cloud}} por meio de uma rede privada, deve-se ter acesso à infraestrutura clássica e ativar roteamento virtual e encaminhamento (VRF) e conectividade com terminais em serviço para sua conta. Em seguida, é possível iniciar a criação de serviços que suportam terminais em serviço para uma conexão de rede privada.
{: shortdesc}

Conclua as etapas a seguir para assegurar-se de que sua conta esteja configurada para criar e usar serviços que suportem terminais em serviço:

1. Verifique se você tem acesso à infraestrutura do {{site.data.keyword.cloud_notm}} em sua conta. Acesse o ícone **Menu** ![ícone Menu](../icons/icon_hamburger.svg) > **Infraestrutura Clássica** para verificar se você tem acesso.
2. Ative sua conta para VRF. Para obter mais informações, consulte [Ativando o roteamento virtual e o encaminhamento](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Ative sua conta para conectividade com terminais em serviço. Para obter mais informações, consulte [Ativando terminais em serviço](/docs/account?topic=account-vrf-service-endpoint#vrf).

Depois de ativar as configurações da conta do VRF e do terminal em serviço, é possível criar recursos a partir do catálogo que suportam terminais de rede privada. A tabela a seguir lista os serviços que suportam o uso de terminais de rede privada. 

Consulte a documentação para o serviço específico para obter mais informações sobre o uso de terminais em serviço.
{: tip}

## Serviços que suportam terminais de rede privada
{: #services-support-service-endpoints}

| Serviço | Documentação |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} integração de terminais em serviço](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} integração de terminais em serviço](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} integração de terminais em serviço](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} integração de terminais em serviço](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} integração de terminais em serviço](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Opções de conectividade](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Conectando-se a um terminal privado](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Incluindo um terminal privado](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Disponível para todos os planos de hardware dedicados implementados após 1 de janeiro de 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}} documentação](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Gerenciando terminais em serviço para o {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Conectando-se ao {{site.data.keyword.keymanagementserviceshort}} na rede privada {{site.data.keyword.cloud_notm}}](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [Documentação do KMIP for VMware on {{site.data.keyword.cloud_notm}}](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Terminais em serviço público e privado para o {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [O {{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) utiliza o terminal em serviço do {{site.data.keyword.keymanagementserviceshort}} para sua integração BYOK|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} integração de terminais em serviço](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Tabela 1. Serviços que suportam o uso de terminais em serviço" caption-side="top"}










