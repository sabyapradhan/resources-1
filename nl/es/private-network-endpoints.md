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

# Configuración de puntos finales de red privada
{: #private-network-endpoints}

Para conectarse a los servicios de {{site.data.keyword.cloud}} a través de una red privada, debe tener acceso a la infraestructura clásica y habilitar el direccionamiento y el reenvío virtuales (VRF) y la conectividad a puntos finales de servicio para su cuenta. A continuación, puede empezar a crear servicios que den soporte a puntos finales de servicio para una conexión de red privada.
{: shortdesc}

Siga los pasos siguientes para asegurarse de que su cuenta está configurada para crear y utilizar servicios que dan soporte a puntos finales de servicio:

1. Compruebe que tiene acceso a la infraestructura de {{site.data.keyword.cloud_notm}} en su cuenta. Vaya al icono de **Menú** ![icono de Menú](../icons/icon_hamburger.svg) > **Infraestructura clásica** para verificar que tiene acceso.
2. Habilite la cuenta para VRF. Para obtener más información, consulte [Habilitación del direccionamiento y el reenvío virtuales](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Habilite la cuenta para que se conecte a los puntos finales de servicio. Para obtener más información, consulte [Habilitación de puntos finales de servicio](/docs/account?topic=account-vrf-service-endpoint#vrf).

Después de habilitar los valores de VRF y de la cuenta de punto final de servicio, puede crear recursos desde el catálogo que den soporte a puntos finales de red privada. En la tabla siguiente se muestran los servicios que dan soporte al uso de puntos finales de red privada. 

Consulte la documentación del servicio específico para obtener más información sobre el uso de puntos finales de servicio.
{: tip}

## Servicios que dan soporte a puntos finales de red privada
{: #services-support-service-endpoints}

| Servicio | Documentación |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [Integración de puntos finales de servicio de {{site.data.keyword.databases-for-elasticsearch}}](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [Integración de puntos finales de servicio de {{site.data.keyword.databases-for-etcd}}](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [Integración de puntos finales de servicio de {{site.data.keyword.databases-for-mongodb}}](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [Integración de puntos finales de servicio de {{site.data.keyword.databases-for-postgresql}}](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [Integración de puntos finales de servicio de {{site.data.keyword.databases-for-redis}}](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Opciones de conectividad](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Conexión con un punto final privado](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Adición de un punto final privado](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Disponible para todos los planes de hardware dedicado desplegados después del 1 de enero de 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [Documentación de {{site.data.keyword.registryshort_notm}}](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Gestión de puntos finales de servicio para {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Conexión con {{site.data.keyword.keymanagementserviceshort}} en la red privada de {{site.data.keyword.cloud_notm}}](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [Documentación de KMIP for VMware on {{site.data.keyword.cloud_notm}}](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Puntos finales de servicio públicos y privados para {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) utiliza el punto final de servicio de {{site.data.keyword.keymanagementserviceshort}} para su integración BYOK|
| {{site.data.keyword.messages-for-rabbitmq}} | [Integración de puntos finales de servicio de {{site.data.keyword.messages-for-rabbitmq}}](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Tabla 1. Servicios que dan soporte al uso de puntos finales de servicio" caption-side="top"}










