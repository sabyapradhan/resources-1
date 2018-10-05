---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Fehlerbehebung für Services und Ressourcen
{: #services}

Zu den Problemen bei einem {{site.data.keyword.Bluemix}}-Service können auch Probleme beim Löschen von Serviceinstanzen gehören. Sie können solche Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}

## Warum kann ich meine Serviceinstanz nicht löschen?
{: #ts_service_broker}

Es kann vorkommen, dass eine Fehlernachricht angezeigt wird, falls Sie versuchen, eine Serviceinstanz zu löschen, die bereits vom Cloud-Controller gelöscht wurde.
{:shortdesc}

Wenn Sie versuchen, eine Serviceinstanz zu löschen, wird die folgende Fehlernachricht angezeigt:
{: tsSymptoms}

`Gateway timeout`

Dieses Problem tritt auf, wenn die Serviceinstanz bereits vom Cloud-Controller gelöscht wurde.
{: tsCauses}

Erstellen Sie eine Serviceinstanz mit demselben Namen und binden Sie sie an Ihre Anwendungen. Anschließend können Sie die Serviceinstanz und die Anwendungen löschen, die den Service verwenden.   
{: tsResolve}
