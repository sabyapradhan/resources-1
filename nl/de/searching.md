---

copyright:

  years: 2015, 2019
lastupdated: "2019-02-18"

keywords: search, find,

subcollection: resources, find resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# Nach Ressourcen suchen
{: #searching-for-resources}

Sie können von einer beliebigen {{site.data.keyword.cloud}}-Konsolenansicht aus nach bereitgestellten Ressourcen suchen, die Sie in der Ressourcenliste und Angeboten im Katalog vermuten. Geben Sie den Namen einer Ressource oder eines Tags in das Suchfeld der Menüleiste der Konsole ein. Sie können Ihre Ressourcen auch über die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle (Command-Line Interface, CLI) durchsuchen. Bei der Befehlszeilenschnittstelle wird standort- und rechenzentrumsübergreifend nach verteilten Anwendungen und Serviceinstanzen gesucht.
{:shortdesc}

## Suchergebnisse verfeinern
{: #results}

<dl>
<dt>Alle Ressourcenergebnisse anzeigen</dt>
<dd>Über diese Option können Sie eine gefilterte Ressourcenliste anzeigen, bei der das Namensfeld in der Ressourcenliste automatisch ausgefüllt wird, sodass Ihnen die relevantesten Ergebnisse angezeigt werden. Als Suchergebnis werden die ersten 10 zurückgegebenen Ergebnisse für Ressourcen angezeigt. Wenn Sie wissen, dass es weitere Ergebnisse gibt, können Sie alle Ergebnisse über die Ressourcenliste anzeigen. Diese Option wird angezeigt, wenn sie zu einem Ressourcenergebnis oder einer Tagsuche passt. Passt die Option nicht zu einem Ressourcennamen oder -tag, wird sie nicht angezeigt.</dd>
<dt>Alle Katalogergebnisse anzeigen</dt>
<dd>Über diese Option können Sie gefilterte Suchergebnisse für den Katalog anzeigen. Es werden die ersten fünf nach Namen geordneten Ergebnisse angezeigt. Wenn detailliertere Suchkriterien für Katalogeinträge verwendet werden sollen, z. B. das Durchsuchen der Beschreibung, können Sie auf diesen Link klicken und eine Ansicht mit gefilterten Katalogergebnissen abrufen. Diese Option beschleunigt die Suche für Angebote, die Sie erstellen möchten. Das Feld wird angezeigt, wenn es zu einem Katalogergebnis passt. Das Feld wird nicht angezeigt, wenn Ihre Suchabfrage mit `tag:` beginnt.</dd>
<dt>Supportfälle durchsuchen</dt>
<dd>Über diese Option können Sie die Ansicht nach Ihren offenen Supportfällen in der gesamten Plattform, Infrastrukturressourcen eingeschlossen, filtern. Die Option wird am Ende der Suche angezeigt, wenn Sie nach einem beliebigen Suchbegriff, `tag:` eingeschlossen, suchen.</dd>
<dt>In Dokumenten suchen</dt>
<dd>Diese Option ermöglicht Ihnen eine gefilterte Ansicht der Dokumentation. Die Option wird am Ende der Suche angezeigt, wenn Sie nach einem beliebigen Suchbegriff, `tag:` eingeschlossen, suchen.</dd>
</dl>

Drücken Sie die Schrägstrichtaste (/), um den Cursor in das Suchfeld zu versetzen.
{: tip}


## Über die Befehlszeilenschnittstelle suchen
{: #searching-cl}

Sie können Ihre gesamten Ressourcen auch unter Verwendung der Lucene-Abfragesyntax durchsuchen. Dazu müssen Sie in der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle einen einzigen Befehl eingeben (gilt ab Version 0.6.7).

  Derzeit unterstützt die Befehlszeilenschnittstelle keine Suche nach Ressourcen, die auf Instanzen der klassischen Infrastruktur ausgeführt werden.
  {: note}

Sie können nach den folgenden Attributen suchen:

<dl>
<dt>`name`</dt>
<dd> Der benutzerdefinierte Name der Ressource.</dd>
<dt>`Region`</dt>
<dd>Der geographische Bereich, in dem die Ressource bereitgestellt wird. Zulässige Werte: `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` und `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>Der Name des Service, wie er in der Spalte 'Name' in der Ausgabe zu 'ibmcloud catalog service-marketplace' erscheint.</dd>
<dt>`family`</dt>
<dd>Die Cloudkomponente, zu der Ihre Ressource gehört. Zulässige Werte: `cloud_foundry`, `containers` und `resource_controller`.</dd>
<dt>`organization_id`</dt>
<dd>Die GUID der Cloud Foundry-Organisation.</dd>
<dt>`doc.space_id`</dt>
<dd>Die GUID des Cloud Foundry-Bereichs.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>Die ID der Ressourcengruppe.</dd>
<dt>`type`</dt>
<dd>Der Ressourcentyp. Zulässige Werte: `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding` und `resource-group`.</dd>
<dt>`creation_date`</dt>
<dd>Das Erstellungsdatum der Ressource.</dd>
<dt>`modification_date`</dt>
<dd> Das Datum, an dem die Ressource zuletzt geändert wurde.</dd>
</dl>

### Suchbeispiele
{: #resource-name}

Die folgenden Beispiele erleichtern die Suche nach Kontoressourcen:

* Suchen Sie nach allen Ressourcen namens `ABC`, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search ‘name:ABC’`

* Suchen Sie nach allen Cloud Foundry-Anwendungen namens `MyResource`, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search 'name:my* AND type:cf-application'`

* Suchen Sie nach allen Message Hub-Serviceinstanzen, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search 'service_name:messagehub'`

* Suchen Sie nach allen Ressourcen in der CLoud Foundry-Organisation `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` oder der Ressourcengruppe `c900d9671b235c00461c5e311a8aeced` in der Region `us-south`, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* Suchen Sie nach allen Ressourcen, die zwischen dem 16. und 20. Mai 2018 erstellt wurden, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`

* Suchen Sie, geordnet nach Ressourcentyp, nach allen Ressourcen, deren Name mit 'my' beginnt, indem Sie den folgenden Befehl eingeben:

    `ibmcloud resource search 'name:my*' -s type`
