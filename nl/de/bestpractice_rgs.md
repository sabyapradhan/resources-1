---

copyright:

  years: 2018
lastupdated: "2018-06-08"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}


# Bewährte Verfahren zum Organisieren von Ressourcen in Ressourcengruppen
{: #bp_resourcegroups}

Ressourcengruppen sind eine Funktion zum Organisieren der [Ressourcen](/docs/resources/acct_resources.html#resource) eines Kontos zu Zugriffssteuerungs- und Abrechnungszwecken. Wenn Sie mit der Verwendung von Cloud Foundry-Bereichen vertraut sind, können Sie sich die Organisation der Ressourcen in Ressourcengruppen auf eine ähnliche Art wie die Organisation der Ressourcen in Bereichen vorstellen. Als Ressourcen werden Elemente bezeichnet, die innerhalb einer Ressourcengruppe erstellt, verwaltet und gespeichert werden können. Benutzer werden nicht zu Ressourcengruppen hinzugefügt. Nur Ressourcen können hinzugefügt werden. 

Derzeit unterstützen nicht alle Services die Verwendung der Zugriffssteuerung {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) und die Zuweisung zu einer Ressourcengruppe. Von IAM verwaltete Services fordern Sie auf, neue Serviceinstanzen zu einer Ressourcengruppe hinzuzufügen, wenn Sie diese in einem Katalog erstellen. Der Zugriff auf die Ressourcen in einer Ressourcengruppe und die Ressourcengruppe selbst werden von IAM verwaltet. Durch die Verwendung von IAM-Rollen können Sie den Benutzern Zugriff auf die Ressourcen bereitstellen, die in Ressourcengruppen zusammengefasst sind. IAM-Rollen können auch die Möglichkeit zum Anzeigen, Bearbeiten und Hinzufügen neuer Serviceinstanzen oder zum Verwalten des Zugriffs auf eine Ressourcengruppe bieten.

Sie können die Liste der von IAM verwalteten Services auch anzeigen, wenn Sie in der IAM-Benutzerschnittstelle Zugriff auf die Ressourcen zuordnen. Wechseln Sie zu **Verwalten** &gt; **Sicherheit** &gt; **Identität und Zugriff**, wählen Sie anschließend einen Benutzer oder eine Service-ID aus und wählen Sie **Zugriff zuweisen** im Menü **Aktionen** aus. Wählen Sie danach **Zugriff auf Ressourcen zuweisen** aus; im Dropdown-Menü **Services** können Sie die Services anzeigen, von denen die Verwendung von IAM unterstützt wird. Für alle Services, von denen die Verwendung von IAM noch nicht unterstützt wird, können Sie weiterhin Cloud Foundry-Organisationen, -Bereiche und -Rollen verwenden. 

Cloud Foundry-Organisationen, -Bereiche und -Rollen unterscheiden sich deutlich von IAM-Rollen. Aus diesem Grund kann von einer Cloud Foundry-Rolle niemals Zugriff auf Ressourcen in einer Ressourcengruppe gewährt werden. 
{: tip}


## Ressourcengruppen einrichten

Alle Benutzer erhalten standardmäßig eine einzelne Benutzergruppe, die umbenannt werden kann. Falls Sie über ein gebührenpflichtiges Konto verfügen, können Sie mehrere Ressourcengruppen zum Organisieren der Ressourcen erstellen. Wenn Sie Ressourcen in unterschiedlichen Ressourcengruppe organisieren, haben Sie folgende Möglichkeiten:

* Zuweisung des Zugriffs auf eine Ressourcengruppe durch Verwendung einer minimalen Anzahl an Richtlinien erleichtern 
* Nach den Nutzungsinformationen der Ressourcengruppen zu Abrechnungszwecken anzeigen 

Führen Sie die folgenden Schritte aus, um eine neue Ressourcengruppe zu erstellen:

1. Rufen Sie **Verwalten** &gt; **Konto** &gt; **Ressourcengruppen** auf.
2. Klicken Sie auf **Ressourcengruppe erstellen**.
3. Geben Sie einen Namen für Ihre Ressourcengruppe ein.
4. Klicken Sie auf **Hinzufügen**.


## Ressourcen zu einer Ressourcengruppe hinzufügen

Services, die mithilfe der IAM-Zugriffssteuerung verwaltet werden, gehören nicht zu einer Organisation oder einem Bereich von Cloud Foundry, sondern zu einer Ressourcengruppe. Wenn Sie eine Serviceinstanz für einen dieser Services aus dem Katalog erstellen, werden Sie aufgefordert, die Instanz einer Ressourcengruppe zuzuweisen. 

**Wichtig**: Ihre Ressourcengruppenauswahl bei der Erstellung der Instanz ist endgültig und kann nicht geändert werden.

Da weitere Services die Zuweisung zu Ressourcengruppen und die Verwendung der IAM-Zugriffssteuerung ermöglichen, werden Sie über das Dashboard benachrichtigt, falls Cloud Foundry-Serviceinstanzen vorhanden sind, die für die Migration ausgewählt werden können. Durch das [Migrieren einer Serviceinstanz zu einer Ressourcengruppe](/docs/resources/instance_migration.html) erstellen Sie eine neue verknüpfte Instanz in einer Ressourcengruppe Ihrer Wahl und die Cloud Foundry-Instanz wird ein Alias. 


## Zugriff auf Ressourcengruppen und die in ihnen enthaltenen Ressourcen zuweisen

Den Zugriff für Benutzer oder Benutzergruppen, die in Zugriffsgruppen organisiert sind, stellen Sie durch die Erstellung von Zugriffsrichtlinien bereit. In Zugriffsrichtlinien wird ein Ziel festgelegt, bei dem es sich in der Regel um eine Serviceinstanz oder alle Instanzen eines Service in einer Ressourcengruppe und einer Rolle handelt, in der definiert ist, welcher Zugriffstyp zulässig ist. Es gibt zwei Arten von Zugriffsrichtlinien, die Sie als Kontoeigner zuweisen müssen, damit die Benutzer in Ihrem Konto über Zugriff auf die Arbeit mit den Ressourcen in den Ressourcengruppen verfügen.

* Zugriff auf Ressourcen in einer Ressourcengruppe. Der Zugriff kann auf alle Ressourcen in einer Gruppe oder nur auf ausgewählte Services in einer Gruppe gewährt werden.
* Zugriff zum Aktivieren der Verwaltung der Gruppen durch die Benutzer; dazu gehört zum Beispiel, dass ein Benutzer eine Gruppe anzeigen, den Gruppennamen bearbeiten, den Zugriff anderer zum Verwalten der Gruppe verwalten und - am wichtigsten - neue Serviceinstanzen erstellen und zu einer Gruppe hinzufügen kann.

Weitere Informationen zu den zwei Arten des Zugriffs und den Möglichkeiten des Benutzers hinsichtlich jeder zugewiesenen IAM-Plattformrolle finden Sie in der folgenden Tabelle:

| Zugriffsrichtlinie - Details  | Aktionen für Zugriff auf Ressourcengruppen | Aktion für Ressourcen in Ressourcengruppen | 
|:-----------------|:--------------|:---------------|
| Zugriff zuweisen für | Ausgewählte Ressourcengruppe | Ausgewählten Service in einer Ressourcengruppe |
| Anzeigeberechtigten-Rolle  | Gruppe und Merkmale, aber nicht Ressourcen in der Gruppe anzeigen | Ressourcen in der Gruppe anzeigen | 
| Operatorrolle | Nicht zutreffend | Nicht zutreffend | 
| Bearbeiterrolle | Name oder Merkmale der Gruppe anzeigen oder bearbeiten, aber nicht der Ressourcen in der Gruppe | Zugriff auf Ressourcen in Ressourcengruppe erstellen, löschen, bearbeiten, aussetzen, wiederaufnehmen, anzeigen, binden und verwalten |
| Administratorrolle |  Zugriff auf Gruppe anzeigen, bearbeiten oder verwalten, aber nicht auf Ressourcen in der Gruppe | Zugriff auf Ressourcen in Ressourcengruppe erstellen, löschen, bearbeiten, aussetzen, wiederaufnehmen, anzeigen, binden und verwalten | 
{: caption="Tabelle 1. Zugriff auf Ressourcengruppen" caption-side="top"}

Wenn ein Benutzer in der Lage sein soll, eine neue Serviceinstanz zu erstellen und diese zu einer Ressourcengruppe hinzufügen zu können, muss dem Benutzer die Rolle eines Anzeigeberechtigten oder eine Rolle mit mehr Berechtigungen für die Ressourcengruppe sowie die Rolle eines Editors (Bearbeiters) für den Service zugewiesen sein.
{: tip}


## Beispiele für Zugriffsrichtlinien

Die folgenden Zugriffsrichtlinienbeispiele sollen die Entscheidung erleichtern, wie der Zugriff auf Ressourcen im Konto zugewiesen soll, die zu Ressourcengruppen gehören.

1. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Administrator' für {{site.data.keyword.Bluemix_notm}} Container Service für das gesamte Konto erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer Zugriff auf alle Instanzen dieses Service und das Erstellen von Serviceinstanzen in allen Ressourcengruppen, für die der Benutzer zumindest über die Rolle eines Anzeigeberechtigten verfügt. Benutzer mit der Rolle eines Administrators für eine Ressource können auch anderen Benutzern Zugriff auf diese Ressource erteilen.
2. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Anzeigeberechtigter' für eine Ressourcengruppe, aber nicht für ihre zugehörigen Ressourcen erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer das Anzeigen der Ressourcengruppe, was zum Erstellen von Instanzen eines Service in dieser Ressourcengruppe erforderlich ist.
3. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Editor' (Bearbeiter) für alle Ressourcen in der Ressourcengruppe erteilt. Ein Benutzer mit der Rolle eines Editors für eine Ressource kann diese Ressource bearbeiten oder löschen.
4. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Administrator' für das gesamte Konto (alle IAM-fähigen Services) erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer das Ausführen von Plattformaktionen für jede Ressource im gesamten Konto und umfasst auch die Fähigkeit zum Ausführen von Verwaltungsaktionen für das Konto, wie zum Beispiel das Verwalten der Ressourcengruppen im Konto.

## Anwendungsfallbeispiele

Falls Sie über eine Gruppe aus Benutzern verfügen, die alle dieselbe Zugriffsebene aufweisen sollen, fügen Sie diese für jeden der obigen Anwendungsfälle zu einer [Zugriffsgruppe](/docs/iam/groups.html#groups) hinzu. Wenn Sie Zugriffsgruppen verwenden, können Sie ein Minimum an Zugriffsrichtlinien verwenden, da alle Mitglieder dieser Zugriffsgruppe die Zugriffsrechte erhalten, die der Gruppe zugewiesen werden.
{: tip}

1. Ich habe ein kleines Konto mit nur 10 Benutzern, die alle gemeinsam an einem einzigen Projekt arbeiten. Einige Benutzer müssen das Konto verwalten und den anderen Benutzern Zugriff zuweisen können. Manche Benutzer müssen Serviceinstanzen bereitstellen können, was Ausgaben verursachen kann. Andere Benutzer sind Anwendungsentwickler, die nur in der Lage sein müssen, die Serviceinstanzen von ihren Anwendungskomponenten zu verwenden. Allen Benutzern müssen unterschiedliche Rollen für das Konto zugewiesen und die Standardressourcengruppe erteilt werden; die Erstellung weiterer Ressourcengruppen zum Aufteilen von Ressourcen oder Beschränken des Zugriffs mancher Benutzer auf bestimmte Ressourcen ist nicht erforderlich. Den Benutzern können die Rollen für das Konto und die Standardbenutzergruppe erteilt werden, die für ihre Bedürfnisse geeignet sind - die Rolle eines Administrators für das Konto für Benutzer, die das Konto verwalten und anderen Zugriff erteilen können müssen, eines Editors für die Standardressourcengruppe und ihre Mitglieder für Benutzer, die Serviceinstanzen bereitstellen können müssen und die Rolle eines Schreibberechtigten (Writer) oder Leseberechtigten (Reader) für Ressourcengruppenmitglieder für Benutzer, die die Serviceinstanzen nur verwenden müssen.
2. Ich habe ein Konto, das aus drei verschiedenen Teams besteht, die an drei Projekten arbeiten. Einige Benutzer sind Administratoren und müssen in der Lage sein, neue Benutzer zum Konto hinzuzufügen, neue Ressourcengruppen zu erstellen und Benutzerzugriff zu Ressourcengruppen hinzuzufügen. Die restlichen Benutzer benötigen nur Zugriff auf die Ressourcengruppe, die ihrem Projekt zugeordnet ist. Ich möchte die Administratorrolle dem Administratorkonto zuordnen. Ich möchte die übrigen Benutzer verschiedenen Rollen für die Ressourcengruppe und Ressourcengruppenmitglieder zuweisen, die dem Projekt zugeordnet sind - die Rolle eines Editors für die Ressourcengruppe für diejenigen, die Instanzen erstellen müssen, und Schreibberechtigter (Writer) bzw. Leseberechtigter (Reader) für die Ressourcengruppenmitglieder, die diese Instanzen verwenden können müssen.
3. Ich habe ein Konto mit mehreren Ressourcengruppen. Ich habe einige Benutzer, die Administratoren für Service A für das gesamte Konto sind und Zugriff auf alle Instanzen dieses Service sowie die Fähigkeit zum Erstellen von Instanzen benötigen; diese Benutzer benötigen jedoch nicht Zugriff auf andere Ressourcen im Konto. Ich möchte diesen Benutzern die Administratorrolle für Service A auf Kontoebene zuweisen und gleichzeitig die Rolle eines Anzeigeberechtigten für alle Ressourcengruppen im Konto zuordnen, für die sie Instanzen erstellen können müssen.
4. Ich habe einen Benutzer in meinem Konto, der nur Zugriff auf eine bestimmte Ressource in einem Service benötigt, zum Beispiel die Fähigkeit zum Schreiben in Bucket A in IBM Cloud Object Storage. Dieser Benutzer darf nicht in der Lage sein, die Ressourcengruppen im Konto anzuzeigen oder auf andere Services oder andere Buckets in dieser Instanz von Cloud Object Storage zuzugreifen. Ich möchte diesem Benutzer die Rolle eines Schreibberechtigten (Writer) für Bucket A in einer bestimmten Instanz von Cloud Object Storage erteilen. Sie können diese Richtlinie entweder mithilfe servicespezifischer Schnittstellen (in diesem Beispiel die Cloud Object Storage-Benutzerschnittstelle) oder der Hauptbenutzerschnittstelle zum Zuweisen von Zugriff erteilen. Es wird empfohlen, die servicespezifische Benutzerschnittstelle zu verwenden, weil hierbei aus einer Liste von Ressourcen ausgewählt werden kann, während in der Benutzerschnittstelle zum Zuweisen von Zugriff keine Ressourcen unterhalb der Serviceinstanzebene angezeigt werden und Sie den CRN-Wert zum Zuweisen der Richtlinie für diese Ressourcen manuell eingeben müssen.
