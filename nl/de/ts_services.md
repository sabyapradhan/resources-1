---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-20"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Fehlerbehebung für Services
{: #services}

Ein {{site.data.keyword.Bluemix}}-Serviceproblem liegt zum Beispiel vor, wenn für ein Gateway ein Zeitlimitfehler auftritt, falls Sie eine Serviceinstanz löschen. Sie können solche Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}

Services in {{site.data.keyword.Bluemix_notm}} können unterschiedliche Typen und Ebenen an Reifegraden aufweisen. So stehen beispielsweise IBM Services und Services von Drittanbietern zur Verfügung und diese Services können Versionen wie 'GA', 'Beta' oder 'Experimentell' aufweisen. Abhängig von Servicetyp und Reifegrad, können unterschiedliche Unterstützungsstufen angeboten werden. Weitere Informationen hierzu finden Sie unter [Unterstützung für Services erhalten](/docs/get-support/servicessupport.html#support-different-services).

## Service-Broker-Fehler beim Löschen einer Serviceinstanz
{: #ts_service_broker}

Es kann vorkommen, dass eine Fehlernachricht angezeigt wird, falls Sie versuchen, eine Serviceinstanz zu löschen, die bereits vom Cloud-Controller gelöscht wurde.
{:shortdesc}

Wenn Sie versuchen, eine Serviceinstanz zu löschen, wird die folgende Service-Broker-Fehlernachricht über eine Gateway-Zeitlimitüberschreitung angezeigt:
{: tsSymptoms}
`Gateway timeout`

Dieses Problem tritt auf, wenn die Serviceinstanz bereits vom Cloud-Controller gelöscht wurde.
{: tsCauses}

Erstellen Sie eine Serviceinstanz mit demselben Namen und binden Sie sie an Ihre Anwendungen. Anschließend können Sie die Serviceinstanz und die Anwendungen löschen, die den Service verwenden.   
{: tsResolve}
