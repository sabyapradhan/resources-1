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

# Serviceendpunkte einrichten
{: #private-network-endpoints}

Wenn Sie eine Verbindung zu {{site.data.keyword.cloud}}-Services über ein privates Netz herstellen möchten, benötigen Sie Zugriff auf die klassische Infrastruktur und müssen VRF sowie die Konnektivität zu Serviceendpunkten für Ihr Konto aktivieren. Dann können Sie mit der Erstellung von Services beginnen, die Serviceendpunkte für eine private Netzverbindung unterstützen.
{: shortdesc}

Führen Sie die folgenden Schritte aus, um sicherzustellen, dass Ihr Konto für die Erstellung und Verwendung von Services, die Serviceendpunkte unterstützen, eingerichtet ist.

1. Stellen Sie sicher, dass Sie über Zugriff auf die {{site.data.keyword.cloud_notm}}-Infrastruktur in Ihrem Konto verfügen. Rufen Sie das **Menüsymbol** ![Menüsymbol](../icons/icon_hamburger.svg) > **Klassische Infrastruktur** auf, um den Zugriff zu verifizieren.
2. Aktivieren Sie das Konto für VRF. Weitere Informationen finden Sie in [VRF aktivieren](/docs/account?topic=account-vrf-service-endpoint#vrf).
3. Aktivieren Sie das Konto für die Konnektivität zu Serviceendpunkten. Weitere Informationen finden Sie in [Serviceendpunkte aktivieren](/docs/account?topic=account-vrf-service-endpoint#service-endpoint).

Nach dem Aktivieren der Kontoeinstellungen für VRF und Serviceendpunkte können Sie über den Katalog Ressourcen erstellen, die Serviceendpunkte unterstützen. In der folgenden Tabelle sind die Services aufgeführt, die die Verwendung von Serviceendpunkten unterstützen.   

Die Dokumentation zum jeweiligen Service enthält weitere Informationen zur Verwendung von Serviceendpunkten.
{: tip}

## Services, die Serviceendpunkte unterstützen
{: #services-support-service-endpoints}

| Service | Dokumentation |
|-------------------|-------------------------------|
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} - Integration von Serviceendpunkten](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} - Integration von Serviceendpunkten](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} - Integration von Serviceendpunkten](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} - Integration von Serviceendpunkten](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} - Integration von Serviceendpunkten](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Konnektivitätsoptionen](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Verbindung zu einem privaten Endpunkt herstellen](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Privaten Endpunkt hinzufügen](/docs/services/EventStreams?topic=eventstreams-manage_endpoints#add_endpoint) |
| {{site.data.keyword.cloudant}}  |  [Verfügbar für alle Pläne für dedizierte Hardware mit einer Bereitstellung nach dem 01. Januar 2019](/docs/services/Cloudant/api?topic=cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | [{{site.data.keyword.registryshort_notm}}-Dokumentation](/docs/services/Registry?topic=va-va_index) |
| {{site.data.keyword.streaminganalyticsfull}} |  [Serviceendpunkte für {{site.data.keyword.streaminganalyticsshort}} verwalten](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Verbindung zu {{site.data.keyword.keymanagementserviceshort}} im privaten {{site.data.keyword.cloud_notm}}-Netz herstellen](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [Dokumentation zu KMIP for VMware on {{site.data.keyword.cloud_notm}}](/docs/services/vmwaresolutions/services?topic=vmware-solutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Öffentliche und private Endpunkte für {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-cs_network_ov#cs_network_ov_master_private) |
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}}](/docs/services/cloud-object-storage?topic=cloud-object-storage-advanced-endpoints) nutzt den Serviceendpunkt von {{site.data.keyword.keymanagementserviceshort}} für die BYOK-Integration|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} - Integration von Serviceendpunkten](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)| 
{: caption="Tabelle 1. Services, die die Verwendung von Serviceendpunkten unterstützen" caption-side="top"}










