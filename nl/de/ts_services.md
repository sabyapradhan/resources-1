---

copyright:

  years: 2015, 2019

lastupdated: "2019-01-28"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Fehlerbehebung für Services und Ressourcen
{: #services}

Allgemeine Probleme mit Services und Ressourcen können Probleme beim Löschen von Serviceinstanzen oder bei der Servicemigration beinhalten. In vielen Fällen können Sie diese Probleme ohne großen Aufwand beheben.
{:shortdesc}

## Warum kann ich meine Serviceinstanz nicht löschen?
{: #ts_service_broker}
{: troubleshoot}

Es kann vorkommen, dass eine Fehlernachricht angezeigt wird, falls Sie versuchen, eine Serviceinstanz zu löschen, die bereits vom Cloud-Controller gelöscht wurde.
{:shortdesc}

Wenn Sie versuchen, eine Serviceinstanz zu löschen, wird die folgende Fehlernachricht angezeigt:
{: tsSymptoms}

`Gateway timeout`

Dieses Problem tritt auf, wenn die Serviceinstanz bereits vom Cloud-Controller gelöscht wurde.
{: tsCauses}

Erstellen Sie eine Serviceinstanz mit demselben Namen und binden Sie sie an Ihre Anwendungen. Anschließend können Sie die Serviceinstanz und die Anwendungen löschen, die den Service verwenden.   
{: tsResolve}

## Warum wurde eine Serviceinstanz in die falsche Ressourcengruppe migriert? 
{: #ts_service_instance}
{: troubleshoot}

Möglicherweise stellen Sie fest, dass eine Serviceinstanz in die falsche Ressourcengruppe migriert wurde und die Zuweisung nicht geändert werden kann. 
{:shortdesc}

Sie können Ressourcen nach dem Zuweisen nicht in eine andere Ressourcengruppe verschieben.
{: tsSymptoms}

Sie haben die Instanz der falschen Ressourcengruppe zugewiesen.  
{: tsCauses}

Dieses Problem können Sie lösen, indem Sie versuchen, die Instanz zu löschen, und eine neue Instanz über den Katalog erstellen. Beim Erstellen können Sie die neue Instanz der richtigen Ressourcengruppe zuweisen.
{: tsResolve}

## Warum kann ich eine infrage kommende Instanz nicht migrieren?
{: #ts_migrate_instance}
{: troubleshoot}

Als ein Benutzer des Kontos haben Sie Probleme beim Migrieren einer infrage kommenden Instanz. 
{:shortdesc}

Sie können eine infrage kommende Instanz nicht migrieren. 
{: tsSymptoms}

Wenn Sie eine infrage kommende Instanz nicht migrieren können, verfügen Sie möglicherweise nicht über den richtigen Zugriff. 
{: tsCauses}

Benutzer müssen über einen bestimmten Zugriff verfügen, um eine Instanz migrieren zu können. Ermitteln Sie Ihre Zugriffsmöglichkeiten, indem Sie in der Menüleiste der Konsole auf **Verwalten** &gt; **Zugriff (IAM)** und anschließend auf **Benutzer** klicken. Klicken Sie auf Ihren Namen und prüfen Sie Ihre Zugriffsrichtlinien auf zugewiesene IAM-Rollen und überprüfen Sie den Cloud Foundry-Zugriff, um die Organisationen, für die Sie über Zugriff verfügen, und die Ihnen zugewiesenen Cloud Foundry-Rollen zu ermitteln. 
{: tsResolve}

## Warum kann ich nicht meine gesamten Services migrieren?
{: #ts_service_migration}
{: troubleshoot}

Eine Migration ist nicht bei allen Services zulässig. 
{:shortdesc}

Sie können bestimmte Services nicht migrieren. 
{: tsSymptoms}

Sie versuchen Services zu migrieren, die nicht für ein Hinzufügen zu Ressourcengruppen infrage kommen und nicht über Identity and Access Management (IAM) verwaltet werden. Wenn ein Service nicht infrage kommt, ist eine Migration nicht möglich. 
{: tsCauses}

Überprüfen Sie die Services, um zu bestätigen, dass eine Migration zulässig ist. Sie erhalten eine Benachrichtigung und können anhand des Flags `support_rc_migration` erkennen, ob ein Service migriert werden kann.
{: tsResolve}
