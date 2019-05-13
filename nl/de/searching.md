---

copyright:

  years: 2015, 2019
lastupdated: "2019-05-08"

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
<dt>In IBM Cloud-Dokumenten suchen</dt>
<dd>Diese Option ermöglicht Ihnen eine gefilterte Suche in der Dokumentation. Die Option wird am Ende der Suche angezeigt, wenn Sie nach einem beliebigen Suchbegriff, `tag:` eingeschlossen, suchen.</dd>
</dl>

Drücken Sie die Schrägstrichtaste (/), um den Cursor in das Suchfeld zu versetzen.
{: tip}


## Über die Befehlszeilenschnittstelle suchen
{: #searching-cl}

Sie können Ihre gesamten Ressourcen auch unter Verwendung der Lucene-Abfragesyntax durchsuchen. Dazu müssen Sie in der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle einen einzigen Befehl eingeben (gilt ab Version 0.6.7).


Sie können nach den folgenden Attributen suchen:

<dl>
<dt>`name`</dt>
<dd> Der benutzerdefinierte Name der Ressource.</dd>
<dt>`Region`</dt>
<dd>Der geographische Bereich, in dem die Ressource bereitgestellt wird. Zulässige Werte: `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` und `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>Der Name des Service, wie er in der Spalte 'Name' in der Ausgabe zu 'ibmcloud catalog service-marketplace' erscheint.</dd>
<dt>`family`</dt>
<dd>Die Cloudkomponente, zu der Ihre Ressource gehört. Die zulässigen Werte sind `cloud_foundry`, `containers`, `vmware`, `resource_controller` oder `ims`.</dd></dd>
<dt>`organization_id`</dt>
<dd>Die GUID der Cloud Foundry-Organisation.</dd>
<dt>`doc.space_id`</dt>
<dd>Die GUID des Cloud Foundry-Bereichs.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>Die ID der Ressourcengruppe.</dd>
<dt>`type`</dt>
<dd>Der Ressourcentyp. Die zulässigen Werte sind `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding`, `resource-group`, `vmware-solutions`, `cloud-object-storage-infrastructure`, `block-storage`, `file-storage`, `cloud-backup`.</dd>
<dt>`creation_date`</dt>
<dd>Das Erstellungsdatum der Ressource.</dd>
<dt>`modification_date`</dt>
<dd> Das Datum, an dem die Ressource zuletzt geändert wurde.</dd>
<dt>`tags`</dt>
<dd>Die Tags, die an die Ressource angehängt wurden. </dd>
<dt>`tagReferences.tag.name`</dt>
<dd>Die Tags, die an eine klassische Infrastrukturressource angehängt wurden. Sie müssen den Parameter `-p classic-infrastructure` angeben. </dd>  
<dt>`_objectType:`</dt>
<dd>Der Objekttyp der klassischen Infrastrukturressource. Zulässige Werte sind: `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest`. Sie müssen den Parameter `-p classic-infrastructure` angeben. </dd> 
</dl>

### Suchbeispiele
{: #resource-name}


Die folgenden Beispiele erleichtern die Suche nach Kontoressourcen:

* Geben Sie den folgenden Befehl ein, um nach allen Ressourcen namens `ABC` zu suchen:
    `ibmcloud resource search ‘name:ABC’`
  
* Geben Sie den folgenden Befehl ein, um nach allen Cloud Foundry-Anwendungen namens `MyResource` zu suchen:

    `ibmcloud resource search 'name:my* AND type:cf-application'`

* Geben Sie den folgenden Befehl ein, um nach allen Serviceinstanzen von Message Hub zu suchen:

    `ibmcloud resource search 'service_name:messagehub'`

* Geben Sie den folgenden Befehl ein, um nach allen Ressourcen entweder in der Cloud Foundry-Organisation `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` oder in der Ressourcengruppe `c900d9671b235c00461c5e311a8aeced` in der Region `us-south` zu suchen:
    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`
    

* Geben Sie den folgenden Befehl ein, um nach Ressourcen zu suchen, die nicht zur klassischen Infrastruktur gehören und die zwischen dem 16. Mai 2018 und dem 20. Mai 2018 erstellt wurden:
    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* Geben Sie den folgenden Befehl ein, um nach Ressourcen zu suchen, die nicht zur klassischen Infrastruktur gehören und deren Name mit "my" beginnt, sortiert nach Typ:

    `ibmcloud resource search 'name:my*' -s type`
    
* Geben Sie den folgenden Befehl ein, um nach Ressourcen zu suchen, die nicht zur klassischen Infrastruktur gehören und die mit dem Tag `MyTag` versehen sind:
    `ibmcloud resource search 'tags:MyTag'`
    
* Geben Sie den folgenden Befehl ein, um nach allen klassischen Infrastrukturressourcen zu suchen, die mit dem Tag `MyTag` versehen sind:
    `ibmcloud resource search 'tagReferences.tag.name:MyTag' -p classic-infrastructure'`
    
* Geben Sie den folgenden Befehl ein, um nach der gesamten klassischen Infrastruktur vom Typ `Softlayer_Hardware` zu suchen:
    `ibmcloud resource search '_objectType:SoftLayer_Hardware' -p classic-infrastructure'`
  

