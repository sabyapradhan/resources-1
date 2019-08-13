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

# Configurazione degli endpoint del servizio
{: #private-network-endpoints}

Per stabilire una connessione ai servizi {{site.data.keyword.cloud}} su una rete privata, devi avere accesso all'infrastruttura classica e abilitare VRF (virtual routing and forwarding) e la connettività agli endpoint del servizio per il tuo account. Puoi quindi iniziare a creare servizi che supportano gli endpoint del servizio per una connessione di rete privata.
{: shortdesc}

Completa la seguente procedura per assicurarti che il tuo account sia impostato per creare e utilizzare servizi che supportano gli endpoint del servizio.

1. Controlla di avere accesso all'infrastruttura {{site.data.keyword.cloud_notm}} nel tuo account. Vai all'icona **Menu** ![Icona Menu](../icons/icon_hamburger.svg) > **Infrastruttura classica** per verificare che disponi dell'accesso.
2. Abilita il tuo account per VRF. Per ulteriori informazioni, vedi [Abilitazione di VRF (virtual routing and forwarding)](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Abilita il tuo account per la connettività agli endpoint del servizio. Per ulteriori informazioni, vedi [Abilitazione degli endpoint del servizio](/docs/account?topic=account-vrf-service-endpoint#service-endpoint).

Dopo che hai abilitato le impostazioni dell'account di VRF ed endpoint del servizio, puoi creare risorse dal catalogo che supportano gli endpoint del servizio. La seguente tabella elenca i servizi che supportano l'utilizzo di endpoint del servizio. 

Fai riferimento alla documentazione per lo specifico servizio per ulteriori informazioni sull'utilizzo degli endpoint del servizio.
{: tip}

## Servizi che supportano endpoint del servizio
{: #services-support-service-endpoints}

| Servizio | Documentazione |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [Integrazione degli endpoint del servizio {{site.data.keyword.databases-for-elasticsearch}}](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [Integrazione degli endpoint del servizio {{site.data.keyword.databases-for-etcd}}](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [Integrazione degli endpoint del servizio {{site.data.keyword.databases-for-mongodb}}](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [Integrazione degli endpoint del servizio {{site.data.keyword.databases-for-postgresql}}](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [Integrazione degli endpoint del servizio {{site.data.keyword.databases-for-redis}}](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Opzioni di connettività](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Connessione a un endpoint privato](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Aggiunta di un endpoint privato](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Disponibile per tutti i piani hardware dedicati distribuiti dopo il 1° gennaio 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [Documentazione di {{site.data.keyword.registryshort_notm}}](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Gestione degli endpoint del servizio per {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Connessione a {{site.data.keyword.keymanagementserviceshort}} sulla rete privata {{site.data.keyword.cloud_notm}}](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP per VMware su {{site.data.keyword.cloud_notm}} | [Documentazione di KMIP per VMware su {{site.data.keyword.cloud_notm}}](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Endpoint del servizio pubblici e privati per {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) utilizza l'endpoint del servizio di {{site.data.keyword.keymanagementserviceshort}} per la sua integrazione BYOK|
| {{site.data.keyword.messages-for-rabbitmq}} | [Integrazione degli endpoint del servizio {{site.data.keyword.messages-for-rabbitmq}}](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Tabella 1. Servizi che supportano l'utilizzo di endpoint del servizio" caption-side="top"}










