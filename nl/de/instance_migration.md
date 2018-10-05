---

copyright:

  years: 2017, 2018

lastupdated: "2018-09-07"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Cloud Foundry-Serviceinstanzen und -Apps in eine Ressourcengruppe migrieren
{: #migrate}

Damit die Arbeit in {{site.data.keyword.Bluemix}} noch einfacher und flexibler wird, wurden [Ressourcengruppen](/docs/resources/resourcegroups.html#rgs) eingeführt, die vom Konzept her Cloud Foundry-Bereichen gleichen. Die Ressourcengruppen zeichnen sich jedoch durch verschiedene Vorteile aus. Sie ermöglichen z. B. eine differenziertere Steuerung mithilfe von IAM (IBM Cloud Identity and Access Management) und Verbindungen zwischen Serviceinstanzen und Apps und Services aus verschiedenen Regionen und bieten eine benutzerfreundliche Möglichkeit, die Verwendung pro Gruppe anzuzeigen.
{:shortdesc}

In einem ersten Schritt werden Services von Cloud Foundry verschoben, damit sie von den Ressourcengruppen profitieren können. Das bedeutet, dass Sie einen Migrationsplan für Ihre Serviceinstanzen oder Apps über den [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://console.bluemix.net/docs/apps/index.html#create) starten müssen, damit sie von ihren aktuellen Cloud Foundry-Organisationen und -Bereichen in eine Ressourcengruppe verschoben werden, wenn das Symbol ![Diese Serviceinstanz zu einer Ressourcengruppe migrieren](images/migrate.svg "Diese Serviceinstanz zu einer Ressourcengruppe migrieren") neben einem Ihrer Services im Dashboard angezeigt wird. Solange ein {{site.data.keyword.Bluemix_notm}}-Service noch Cloud Foundry-Organisationen, -Bereiche und -Rollen und nicht IAM und Ressourcengruppen verwendet, können Sie vorhandene Cloud Foundry-Serviceinstanzen nicht zu Ressourcengruppen migrieren.

Wenn Sie vorhandene Cloud Foundry-Serviceinstanzen oder {{site.data.keyword.dev_console}}-Apps zu einer Ressourcengruppe migrieren, kann die ausgewählte Gruppe nicht mehr geändert werden, nachdem die Migration abgeschlossen ist. Deswegen ist es wichtig, vor der Migration zu planen, wie Sie Ressourcen im Konto organisieren möchten. Dies könnte bedeuten, dass Sie vor der Migration eine oder mehrere Ressourcengruppen erstellen müssen, wenn Sie ein abrechnungsfähiges Konto haben. 

Sie können versuchen, Ihre Ressourcen in Ressourcengruppen zu organisieren, genauso wie Sie Ressourcen in Cloud Foundry-Bereichen organisiert haben. Weitere Informationen zur Verwendung von Ressourcengruppen finden Sie unter [Bewährte Verfahren für die Organisation von Ressourcen in Ressourcengruppen](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).
{: tip}


## Welche Vorteile bringt die Migration?

### Cloud Foundry-Serviceinstanzen

Services, die die Cloud IAM-Zugriffssteuerung und -Organisation innerhalb von Ressourcengruppen unterstützen, bieten verschiedene Vorteile:

* Mithilfe der differenzierten Zugriffssteuerung können Sie den Zugriff auf einzelne Serviceinstanzen oder eine Gruppe aus Ressourcen festlegen, die in einer Ressourcengruppe organisiert sind. 
* Mithilfe von Zugriffsgruppen und Ressourcengruppen zum Organisieren von Benutzern und Ressourcen legen Sie nur eine Mindestanzahl an Zugriffsrichtlinien fest. Wenn Sie zum Beispiel über eine Reihe von Entwicklern verfügen, die alle über Zugriff auf Ressourcen für eine Entwicklungsumgebung erhalten sollen, können Sie all diese Benutzer in einer Entwicklerzugriffsgruppe organisieren und anschließend alle Ressourcen zu einer einzigen Ressourcengruppe hinzufügen, auf die sie Zugriff benötigen. Danach können Sie eine einzige Richtlinie für die Zugriffsgruppe definieren, damit sie über Zugriff auf alle Ressourcen in der Ressourcengruppe verfügen.
* Sie können die Verwendung ähnlich wie bei Cloud Foundry-Organisationen nach Ressourcengruppe anzeigen.
* Sie können Verbindungen zu Apps und Services in einem beliebigen Cloud Foundry-Bereich herstellen, was Verbindungen für Apps und Services aus unterschiedlichen Regionen ermöglicht. Wenn Sie die Migration ausführen, wird die Verbindung automatisch hergestellt, indem Sie Ihre ursprüngliche Cloud Foundry-Serviceinstanz in einen Alias umwandeln und in einer Ressourcengruppe Ihrer Wahl eine verknüpfte Instanz erstellen. In der folgenden Abbildung wird dargestellt, wie die Verbindung mithilfe eines Alias funktioniert.

![Serviceinstanz an einen Cloud Foundry-Bereich binden, um einen Alias zu erstellen](images/alias.svg "Serviceinstanz an einen Cloud Foundry-Bereich binden, um einen Alias zu erstellen")

### {{site.data.keyword.dev_console}}apps

Bisher konnten {{site.data.keyword.dev_console}}-Apps nur Cloud Foundry-Serviceinstanzen zugeordnet werden. Jetzt können Sie Ihre Apps zu Serviceinstanzen zuordnen, die zu einer Ressourcengruppe gehören und die Zugriffssteuerung über Cloud IAM unterstützen, wenn Sie Ihre Apps zu einer Ressourcengruppe migrieren. 

## Wer kann die Migration durchführen?
{: #whocanmigrate}

### Erforderlicher Zugriff für Serviceinstanzen 

Benutzer müssen über bestimmte Zugriffsrechte verfügen, um Cloud Foundry-Serviceinstanzen in eine Ressourcengruppe zu migrieren:

* Einem Benutzer muss die Entwicklerrolle des Cloud Foundry-Bereichs oder die Cloud Foundry-Rolle eines Organisationsmanagers für die Organisation zugeordnet sein, zu der die Instanz gehört.
* Einem Benutzer muss mindestens die IAM-Rolle eines Anzeigeberechtigten zugeordnet sein, um die Ressourcengruppe verwalten zu können, zu der die Instanz migriert wird.
* Einem Benutzer muss mindestens die IAM-Rolle eines Bearbeiters für den Service zugeordnet sein.

Weitere Informationen zum Zuordnen des korrekten Zugriffs finden Sie unter [Cloud Foundry-Zugriff](/docs/iam/cfaccess.html#cfaccess) und [IAM-Zugriff](/docs/iam/users_roles.html#platformrolestable).

Finden Sie heraus, welchen Zugriff Sie haben, indem Sie in der Menüleiste der Konsole auf **Verwalten** &gt; **Sicherheit** &gt; **Identität und Zugriff** und anschließend auf **Benutzer** klicken. Klicken Sie auf Ihren Namen und prüfen Sie Ihre **Zugriffsrichtlinien** für zugewiesene IAM-Rollen und den **Cloud Foundry-Zugriff**, um die Organisationen, auf die Sie Zugriff haben, und Ihre zugeordneten Cloud Foundry-Rollen anzuzeigen.
{: tip}

### Erforderlicher Zugriff für {{site.data.keyword.dev_console}}-Apps

Benutzer, die auf eine {{site.data.keyword.dev_console}}-App zugreifen können, können die App migrieren. Beim Migrieren einer App werden jedoch nicht die zu der App gehörigen Services migriert. Serviceinstanzen müssen separat migriert werden.

## Wie funktioniert Migration?

### Serviceinstanzen migrieren

Bei der Migration einer Serviceinstanz aus einer Cloud Foundry-Organisation und einem Cloud Foundry-Bereich zu einer Ressourcengruppe wird eine neue verknüpfte Serviceinstanz in der Ressourcengruppe erstellt. Die ursprüngliche Instanz in der Cloud Foundry-Organisation und dem Cloud Foundry-Bereich wird zu einem [Aliasnamen](/docs/resources/connecting_apps.html#what_is_alias). Der Alias wird zum Quota Ihrer Organisation hinzugezählt, aber Ihnen wird die Verwendung der Serviceinstanz in der Ressourcengruppe in Rechnung gestellt.

![Migration einer Cloud Foundry-Serviceinstanz zu einer Ressourcengruppe](images/migration.gif){: gif}

Die Serviceinstanzen werden nacheinander migriert, wenn Sie im Dashboard über das Symbol ![Diese Serviceinstanz zu einer Ressourcengruppe migrieren](images/migrate.svg "Diese Serviceinstanz zu einer Ressourcengruppe migrieren") benachrichtigt werden, das Ihrer Cloud Foundry-Serviceinstanz zugeordnet ist.

Ziehen Sie vor dem Start des Migrationsprozesses die Servicedokumentation zu Rate, um zu überprüfen, ob Sie eventuell zusätzliche servicespezifische Änderungen durchführen müssen, wenn Sie die Serviceinstanz zu einer Ressourcengruppe migrieren. Es kann zum Beispiel erforderlich sein, Daten von alten Instanzen zu neuen Instanzen zu migrieren oder die für eine App verwendeten Berechtigungsnachweise zu aktualisieren, wenn Sie den Cloud Foundry-Alias löschen. Für Anwendungen, von denen ein Direktaufruf eines Service ausgeführt wird, der migriert wurde, muss der API-Aufruf so aktualisiert werden, dass entweder ein IAM-API-Schlüssel oder -Zugriffstoken verwendet wird.
{: tip}

1. Öffnen Sie das Menü **Weitere Aktionen**.
2. Wählen Sie **Zu einer Ressourcengruppe migrieren** aus, um den Prozess zu starten.
3. Wählen Sie eine Ressourcengruppe aus.
4. Klicken Sie auf **Migrieren** und die Instanz wird für Sie migriert.
5. Da Sie immer nur eine Instanz migrieren können, können Sie weitere infrage kommende Instanzen migrieren, nachdem die erste erfolgreich abgeschlossen wurde.

Nachdem Sie eine Instanz erfolgreich migriert haben, wird sie im Bereich 'Services' Ihres Dashboards angezeigt. Der Aliasname verbleibt im Abschnitt 'Cloud Foundry' des Dashboards. Sie können den Link ![Linksymbol](images/link.svg "Linksymbol für einen Alias") im Cloud Foundry-Abschnitt des Dashboards verwenden, um die Aliase zu ermitteln.

### {{site.data.keyword.dev_console}}-Apps migrieren

Apps werden einzeln nacheinander migriert. Klicken Sie dazu auf das Symbol ![Diese Serviceinstanz zu einer Ressourcengruppe migrieren](images/migrate.svg "Diese Serviceinstanz zu einer Ressourcengruppe migrieren") neben den einzelnen Einträgen in der Ansicht mit der Anwendungsliste.

1. Wählen Sie das Symbol **Menü** ![Menüsymbol](../icons/icon_hamburger.svg) und danach das gewünschte Entwicklerportal, z. B. Watson, Mobile oder Web Apps, aus.
2. Wählen Sie **Apps** aus. Daraufhin werden die Listen **Apps (Aktion erforderlich)** und **Apps (migriert)** angezeigt.
3. Klicken Sie für jeden Eintrag in der Liste **Apps (Aktion erforderlich)** auf das Symbol **Migrieren** ![Diese Serviceinstanz zu einer Ressourcengruppe migrieren](images/migrate.svg "Diese Serviceinstanz zu einer Ressourcengruppe migrieren").
4. Wählen Sie eine Ressourcengruppe aus oder erstellen Sie eine neue Ressourcengruppe.
5. Klicken Sie auf **Migrieren**. Die App wird für Sie migriert.
6. Vergewissern Sie sich, dass die App nun in der Liste **Apps (migriert)** angezeigt wird.
7. Da Sie immer nur eine App migrieren können, können Sie fortfahren, indem Sie weitere gewünschte Apps nach der ersten App migrieren.


## Nächste Schritte

Nach der Migration einer Cloud Foundry-Serviceinstanz zu einer Ressourcengruppe müssen Sie sicherstellen, dass die Benutzer im Konto über die erforderliche Zugriffsebene für die Ressourcen in den Ressourcengruppen des Kontos verfügen. Es kann auch sinnvoll sein, Zugriff zum Verwalten der Ressourcengruppe zu ermöglichen, damit die Benutzer neue Serviceinstanzen in den Ressourcengruppen des Kontos erstellen können.

Weitere Informationen zum Zuordnen des Zugriffs auf Ressourcen in Ressourcengruppen finden Sie unter [Zugriff auf Ressourcengruppen und die in ihnen enthaltenen Ressourcen zuweisen](/docs/resources/bestpractice_rgs.html#assigning-access-to-resource-groups-and-the-resources-within-them).

Überprüfen Sie anhand der Dokumentation für den Service auch, ob im Anschluss an die Migration Aktualisierungen für die vorhandenen Apps ausgeführt werden müssen. 


## Fehlerbehebung

Wenn bei der Migration von Cloud Foundry-Serviceinstanzen Probleme auftreten, finden Sie weitere Informationen unter [Fehlerbehebung für die Migration von Serviceinstanzen](/docs/resources/ts_migration.html).
