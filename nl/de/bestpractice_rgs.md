---

copyright:

  years: 2018
lastupdated: "2018-01-09"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Bewährte Verfahren zum Organisieren von Ressourcen in Ressourcengruppen
{: #bp_resourcegroups}

Eine Ressourcengruppe bietet Ihnen die Möglichkeit, Ihre Konto[ressourcen](/docs/resources/acct_resources.html#resource) nach Zugriffssteuerungs- und Abrechnungskriterien zusammenzufassen. Wenn Sie mit der Verwendung von Cloud Foundry-Bereichen vertraut sind, können Sie sich die Zusammenfassung von Ressourcen in Ressourcengruppen wie die Zusammenfassung von Ressourcen in Bereichen vorstellen. Als Ressourcen werden Elemente bezeichnet, die innerhalb einer Ressourcengruppe erstellt, verwaltet und gespeichert werden können. Benutzer werden nicht zu Ressourcengruppen hinzugefügt. Nur Ressourcen können hinzugefügt werden. 

Derzeit unterstützen nicht alle Services die Verwendung der Zugriffssteuerung {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) und die Zuweisung zu einer Ressourcengruppe. IAM-fähige Services fordern Sie auf, neue Serviceinstanzen zu einer Ressourcengruppe hinzuzufügen, wenn Sie diese über den Katalog erstellen. Der Zugriff auf die Ressourcen in einer Ressourcengruppe und die Ressourcengruppe selbst wird von IAM verwaltet. Durch die Verwendung von IAM-Rollen können Sie den Benutzern Zugriff auf die Ressourcen bereitstellen, die in Ressourcengruppen zusammengefasst sind. IAM-Rollen können auch die Möglichkeit zum Anzeigen, Bearbeiten und Hinzufügen neuer Serviceinstanzen oder zum Verwalten des Zugriffs auf eine Ressourcengruppe bieten.

Sie können die Liste der IAM-fähigen Services auch anzeigen, wenn Sie in der IAM-Benutzerschnittstelle wie folgt Zugriff auf Ressourcen zuweisen:
1. Rufen Sie **Verwalten** &gt; **Zugriff (IAM)** auf und wählen Sie dann **Benutzer** aus. 
2. Wählen Sie einen Benutzernamen aus und klicken Sie auf **Zugriffsrichtlinien**. 
3. Wählen Sie **Zugriff zuweisen** > **Zugriff zu Ressourcen zuweisen** aus.
4. Wählen Sie über das Menü **Services** den Service aus, der zugewiesen werden soll. Für alle Services, die die Verwendung von IAM noch nicht unterstützen, können Sie weiterhin Cloud Foundry-Organisationen, -Bereiche und -Rollen verwenden. 
5. Klicken Sie auf **Zuweisen**.

Cloud Foundry-Organisationen, -Bereiche und -Rollen unterscheiden sich deutlich von IAM-Rollen. Über eine Cloud Foundry-Rolle kann niemals Zugriff auf Ressourcen in einer Ressourcengruppe erteilt werden. 
{: note}


## Ressourcengruppen einrichten

Alle Benutzer erhalten standardmäßig eine einzelne Benutzergruppe, die umbenannt werden kann. Weisen Sie die Rolle des Bearbeiters oder des Administrators dem Gültigkeitsbereich 'Alle Kontoverwaltungsservices' zu, um Ressourcengruppen zu erstellen. Falls Sie über ein gebührenpflichtiges Konto verfügen, können Sie mehrere Ressourcengruppen zum Organisieren der Ressourcen erstellen. Wenn Sie Ressourcen in unterschiedlichen Ressourcengruppen zusammenfassen, eröffnen sich folgende Möglichkeiten:

* Zuweisung des Zugriffs auf eine Ressourcengruppe durch Verwendung einer minimalen Anzahl an Richtlinien erleichtern 
* Anzeigen von Ressourcengruppen nach Nutzungsinformationen der Ressourcengruppen zu Abrechnungszwecken 

Führen Sie die folgenden Schritte aus, um eine neue Ressourcengruppe zu erstellen:

1. Rufen Sie **Verwalten** > **Konto** auf. 
2. Erweitern Sie den Eintrag **Kontoressourcen** und wählen Sie **Ressourcengruppen** aus. 
3. Klicken Sie auf **Ressourcengruppe erstellen**.
4. Geben Sie einen Namen für Ihre Ressourcengruppe ein.
5. Klicken Sie auf **Hinzufügen**.


## Ressourcen zu einer Ressourcengruppe hinzufügen

Services, die über die IAM-Zugriffssteuerung aktiviert werden, gehören nicht zu einer Organisation oder einem Bereich von Cloud Foundry, sondern zu einer Ressourcengruppe. Wenn Sie eine Serviceinstanz für einen dieser Services über den Katalog erstellen, werden Sie aufgefordert, die Instanz einer Ressourcengruppe zuzuweisen. 

**Wichtig**: Ihre Ressourcengruppenauswahl bei der Erstellung der Instanz ist endgültig und kann nicht geändert werden.

Da die Zahl der Services, die die Zuweisung zu Ressourcengruppen und die Verwendung der IAM-Zugriffssteuerung ermöglichen, zunimmt, werden Sie auf der Ressourcenliste benachrichtigt, falls Cloud Foundry-Serviceinstanzen vorhanden sind, die für die Migration ausgewählt werden können. Durch das [Migrieren einer Serviceinstanz zu einer Ressourcengruppe](/docs/resources/instance_migration.html) erstellen Sie eine neue verknüpfte Instanz in einer Ressourcengruppe Ihrer Wahl und die Cloud Foundry-Instanz wird zu einem Alias. 


## Zugriff auf Ressourcengruppen und die in ihnen enthaltenen Ressourcen zuweisen

Den Zugriff für Benutzer oder Benutzergruppen, die zu Zugriffsgruppen zusammengefasst sind, stellen Sie durch die Erstellung von Zugriffsrichtlinien bereit. In Zugriffsrichtlinien wird ein Ziel festgelegt, bei dem es sich in der Regel um eine Serviceinstanz oder alle Instanzen eines Service in einer Ressourcengruppe handelt, sowie eine Rolle, die den zulässigen Zugriffstyp definiert. Es gibt zwei Arten von Zugriffsrichtlinien, die Sie als Kontoeigner zuweisen müssen, damit die Benutzer in Ihrem Konto über den nötigen Zugriff für die Arbeit mit den Ressourcen in den Ressourcengruppen verfügen.

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

Wenn ein Benutzer neue Serviceinstanz erstellen und diese zu einer Ressourcengruppe hinzufügen können soll, muss dem Benutzer die Rolle eines Anzeigeberechtigten oder eine Rolle mit umfassenderen Berechtigungen für die Ressourcengruppe sowie die Rolle eines Editors (Bearbeiters) für den Service zugewiesen werden.
{: tip}


## Beispiele für Zugriffsrichtlinien

Die folgenden Zugriffsrichtlinienbeispiele sollen die Entscheidung erleichtern, wie der Zugriff auf Ressourcen im Konto zugewiesen soll, die zu Ressourcengruppen gehören.

1. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Administrator' für {{site.data.keyword.Bluemix_notm}} Container Service für das gesamte Konto erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer Zugriff auf alle Instanzen dieses Service und das Erstellen von Serviceinstanzen in allen Ressourcengruppen, für die der Benutzer zumindest über die Rolle eines Anzeigeberechtigten verfügt. Benutzer mit der Rolle eines Administrators für eine Ressource können auch anderen Benutzern Zugriff auf diese Ressource erteilen.
2. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Anzeigeberechtigter' für eine Ressourcengruppe, aber nicht für ihre zugehörigen Ressourcen erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer das Anzeigen der Ressourcengruppe, was zum Erstellen von Instanzen eines Service in dieser Ressourcengruppe erforderlich ist.
3. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Editor' (Bearbeiter) für alle Ressourcen in der Ressourcengruppe erteilt. Ein Benutzer mit der Bearbeiterrolle für eine Ressource kann diese Ressource bearbeiten oder löschen.
4. Eine Richtlinie, die dem Benutzer die Plattformrolle 'Administrator' für das gesamte Konto (alle IAM-fähigen Services) erteilt. Eine Richtlinie mit diesen Details ermöglicht dem Benutzer das Ausführen von Plattformaktionen für jede Ressource im gesamten Konto und umfasst auch die Fähigkeit zum Ausführen von Verwaltungsaktionen für das Konto, wie zum Beispiel das Verwalten der Ressourcengruppen im Konto.

## Anwendungsfallbeispiele

Falls Sie über eine Gruppe aus Benutzern verfügen, die alle dieselbe Zugriffsebene aufweisen sollen, fügen Sie diese für jeden der obigen Anwendungsfälle zu einer [Zugriffsgruppe](/docs/iam/groups.html#groups) hinzu. Wenn Sie Zugriffsgruppen verwenden, können Sie ein Minimum an Zugriffsrichtlinien verwenden, da alle Mitglieder der Zugriffsgruppe alle Zugriffsrechte erhalten, die der Gruppe zugewiesen sind.
{: tip}

<ol>
<li><p>Ich habe ein kleines Konto mit nur 10 Benutzern, die alle gemeinsam an einem einzigen Projekt arbeiten. Einige Benutzer müssen das Konto verwalten und den anderen Benutzern Zugriff zuweisen. Manche Benutzer müssen Serviceinstanzen bereitstellen, wodurch Ausgaben verursacht werden. Andere Benutzer sind Anwendungsentwickler, die lediglich die Serviceinstanzen von ihren Anwendungskomponenten aus verwenden.</p>
<p>Allen Benutzern müssen unterschiedliche Rollen für das Konto zugewiesen und die Standardressourcengruppe erteilt werden; die Erstellung weiterer Ressourcengruppen zum Aufteilen von Ressourcen oder Beschränken des Zugriffs mancher Benutzer auf bestimmte Ressourcen ist nicht erforderlich. Den Benutzern können die Rollen für das Konto und die Standardbenutzergruppe erteilt werden, die für ihre Bedürfnisse geeignet sind - die Rolle eines Administrators für das Konto für Benutzer, die das Konto verwalten und anderen Zugriff erteilen müssen, eines Editors für die Standardressourcengruppe und die zugehörigen Mitglieder für Benutzer, die Serviceinstanzen bereitstellen müssen, und die Rolle eines Schreibberechtigten oder Leseberechtigten für Ressourcengruppenmitglieder für Benutzer, die die Serviceinstanzen nur verwenden.</p>
</li>
<li><p>Ich habe ein Konto, das aus drei verschiedenen Teams besteht, die an drei Projekten arbeiten. Einige Benutzer sind Administratoren und müssen in der Lage sein, neue Ressourcengruppen zu erstellen und Benutzerzugriff zu Ressourcengruppen hinzuzufügen. Die restlichen Benutzer benötigen nur Zugriff auf die Ressourcengruppe, die ihrem Projekt zugeordnet ist.</p>
<p>Den Administratoren sollte die Administratorrolle für alle IAM-fähigen Services zugewiesen werden. Den übrigen Benutzern sollten verschiedenen Rollen für die Ressourcengruppe und Ressourcengruppenmitglieder zugewiesen werden, die dem Projekt zugeordnet sind - die Rolle eines Editors für die Ressourcengruppe für diejenigen, die Instanzen erstellen müssen, und Schreibberechtigter bzw. Leseberechtigter für die Benutzer, die Instanzen verwenden können müssen.</p>
</li>
<li><p>Ich habe ein Konto mit mehreren Ressourcengruppen. Ich habe einige Benutzer, die Administratoren für Service A für das gesamte Konto sind und Zugriff auf alle Instanzen dieses Service sowie die Fähigkeit zum Erstellen von Instanzen benötigen; diese Benutzer benötigen jedoch nicht Zugriff auf andere Ressourcen im Konto.</p>
<p>Diesen Benutzern sollte die Administratorrolle für Service A auf Kontoebene und gleichzeitig die Rolle eines Anzeigeberechtigten für alle Ressourcengruppen im Konto zugewiesen werden, für die sie Instanzen erstellen können müssen.</p>
</li>
<li><p>Ich habe einen Benutzer in meinem Konto, der nur Zugriff auf eine bestimmte Ressource in einem Service benötigt, zum Beispiel die Fähigkeit zum Schreiben in Bucket A in IBM Cloud Object Storage. Dieser Benutzer sollte nicht die Ressourcengruppen im Konto anzeigen oder auf andere Services oder andere Buckets in dieser Instanz von Cloud Object Storage zugreifen können.</p> 
<p>Diesem Benutzer sollte die Rolle eines Schreibberechtigten für Bucket A in einer bestimmten Instanz von Cloud Object Storage erteilt werden. Sie können diese Richtlinie entweder mithilfe servicespezifischer Schnittstellen (in diesem Beispiel die Cloud Object Storage-Benutzerschnittstelle) oder der Hauptbenutzerschnittstelle zum Zuweisen von Zugriff erteilen. Es wird empfohlen, die servicespezifische Benutzerschnittstelle zu verwenden, weil hierbei aus einer Liste von Ressourcen ausgewählt werden kann, während in der Benutzerschnittstelle zum Zuweisen von Zugriff keine Ressourcen unterhalb der Serviceinstanzebene angezeigt werden und Sie den CRN-Wert zum Zuweisen der Richtlinie für diese Ressourcen manuell eingeben müssen.</p>
</li>
<li><p>Ich verwende zurzeit Cloud Foundry-Organisationen und -Bereiche, möchte jedoch mit der Verwendung von Ressourcengruppen und Zugriffsgruppen für meine IAM-fähigen Services beginnen. Zum gegenwärtigen Zeitpunkt sind Benutzer und Ressourcen in Organisationen für bestimmte Geschäftsbereiche zusammengefasst; die Bereiche werden für verschiedene Projekte innerhalb eines Geschäftsbereichs verwendet.</p>
<p>Die Ressourcen sollten auf dieselbe Weise in den Ressourcengruppen zusammengefasst werden wie bisher in den Bereichen, wobei jede Ressourcengruppe einen Projektbereich darstellen soll. Dann sollten separate Zugriffsgruppen eingerichtet werden, um den Benutzern die erforderlichen Zugriffsberechtigungen für die entsprechenden Ressourcengruppen auf Projektebene zu erteilen. Dabei kann der Zugriff für alle Ressourcen in einer Ressourcengruppe oder für ausgewählte Ressourcen innerhalb einer Ressourcengruppe erteilt werden. So kann jede Zugriffsgruppe mit unterschiedlichen Zugriffsebenen für Ressourcen innerhalb einer Ressourcengruppe eingerichtet werden, wodurch jede Benutzergruppe die Zugriffsberechtigungen erhält, die die Benutzer für die Arbeit mit den Ressourcen oder mit der Ressourcengruppe selbst benötigen.</p>
</li>
</ol>


