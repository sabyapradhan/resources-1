---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Sicherer Zugriff auf Services mit Serviceendpunkten
{: #service-endpoints}

Für Kunden, die cloudbasierte Services für Produktionsworkloads verwenden, hat die Sicherheit eine immer höhere Priorität. Der sichere Zugriff auf Services ist für viele Kunden nicht nur eine vernünftige Unternehmenspolitik, sondern in einigen Fällen auch eine Voraussetzung im Rahmen von Compliance-Vorgaben. {{site.data.keyword.IBM_notm}} hat die Konnektivitätsoptionen für Kunden erweitert, die für ihre Workloads die Möglichkeit einer isolierten Konnektivität benötigen. 

Mit {{site.data.keyword.cloud}}-Serviceendpunkten können Verbindungen zu {{site.data.keyword.cloud_notm}}-Services über das private {{site.data.keyword.cloud_notm}}-Netz hergestellt werden. Das Verlagern dieser Workloads vom öffentlichen zum privaten Netz bietet zwei Vorteile:

* Services werden nicht mehr über eine Internet-Routing-fähige IP-Adresse verarbeitet. Zu den Anforderungen von Cloud-Kunden gehört immer häufiger, dass über ihre Services kein oder nur eingeschränkter Zugriff auf das öffentliche Internet möglich sein soll. Mit dem Serviceendpunktfeature können Service-Teams nun über das private Netz eine Schnittstelle für ihren Service erstellen, die Kunden zur Verbindungsherstellung verwenden können. Internetzugriff ist keine Voraussetzung mehr für die Herstellung von Verbindungen zu {{site.data.keyword.cloud_notm}}-Services.
* Im privaten Netz gibt es keine abrechnungsfähigen oder nutzungsabhängigen Gebühren für Bandbreiten. Bisher sind bei der Kommunikation mit einem {{site.data.keyword.cloud_notm}}-Service Gebühren für die Bandbreitenbelegung in ausgehender Richtung angefallen. 

In der folgenden Abbildung ist das Routing des Datenverkehrs durch das private Netz von {{site.data.keyword.cloud_notm}} beim Zugriff auf Cloud-Services über Serviceendpunkte dargestellt:

![IBM Cloud-Serviceendpunkt](images/CSE.png "Routing des Datenverkehrs über einen Serviceendpunkt")

Für die Verwendung von {{site.data.keyword.cloud_notm}}-Serviceendpunkten müssen Sie VRF in Ihrem Konto aktivieren.  Anschließend können Sie die Verwendung von Serviceendpunkten aktivieren. Nach dem Aktivieren beider Optionen können Sie mit der Erstellung von Services aus dem Katalog beginnen, die die Verwendung von VRF und Serviceendpunkten unterstützen. Weitere Informationen finden Sie in [VRF und Serviceendpunkte aktivieren](/docs/account?topic=account-vrf-service-endpoint).
