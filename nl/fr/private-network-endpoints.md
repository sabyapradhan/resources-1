---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

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

# Configuration de noeuds finaux de service
{: #private-network-endpoints}

Pour vous connecter aux services {{site.data.keyword.cloud}} sur un réseau privé, vous devez avoir accès à l'infrastructure classique et activer la fonction de routage et transfert virtuel (VRF), ainsi que la connectivité aux noeuds finaux de service pour votre compte. Vous pouvez ensuite commencer à créer des services qui prennent en charge les noeuds finaux de service pour une connexion de réseau privé.
{: shortdesc}

Pour s'assurer que votre compte est configuré pour créer et utiliser des services compatibles avec les noeuds finaux de service, procédez comme suit :

1. Vérifiez que vous avez accès à l'infrastructure {{site.data.keyword.cloud_notm}} dans votre compte. Accédez à l'icône **Menu** ![Icône Menu](../icons/icon_hamburger.svg) > **Infrastructure classique** pour vérifier que vous disposez de l'accès.
2. Activez votre compte pour le routage et le transfert virtuel (VRF). Pour plus d'informations, voir [Activation de VRF](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Activez votre compte pour la connectivité avec les noeuds finaux de service. Pour plus d'informations, voir [Activation des noeuds finaux de service](/docs/account?topic=account-vrf-service-endpoint#service-endpoint).

Après avoir activé les paramètres du compte pour VRF et les noeuds finaux de service, vous pouvez créer des ressources compatibles avec les noeuds finaux de service à partir du catalogue. 
Le tableau suivant répertorie les services qui prennent en charge l'utilisation des noeuds finaux de service. 

Consultez la documentation spécifique au service pour obtenir plus d'informations sur l'utilisation des noeuds finaux de service.
{: tip}

## Services qui prennent en charge les noeuds finaux de service
{: #services-support-service-endpoints}

| Service | Documentation |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} service endpoints integration](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} service endpoints integration](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} service endpoints integration](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} service endpoints integration](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} service endpoints integration](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Options de connectivité](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Connexion à un noeud final privé](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Adding a private endpoint](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Available for all dedicated hardware plans deployed after 1 January 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [Documentation d'{{site.data.keyword.registryshort_notm}}](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Managing service endpoints for {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Connecting to {{site.data.keyword.keymanagementserviceshort}} on the {{site.data.keyword.cloud_notm}} private network](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [Documentation de KMIP for VMware on {{site.data.keyword.cloud_notm}}](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Public and private service endpoints for {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) utilizes {{site.data.keyword.keymanagementserviceshort}}'s service endpoint for its BYOK integration|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} service endpoints integration](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Tableau 1. Services compatibles avec l'utilisation des noeuds finaux de service" caption-side="top"}










