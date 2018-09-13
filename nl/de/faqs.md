---

copyright:

  years: 2015, 2018
  
lastupdated: "2018-08-29"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Häufig gestellte Fragen (FAQs)
{: #resources-faq}

## Was ist eine Ressourcengruppe?
{: #resource-group}

Eine Ressourcengruppe bietet Ihnen die Möglichkeit, Ihre Kontoressourcen in anpassbaren Gruppierungen zu organisieren. Jede Kontoressource, die mit der Zugriffssteuerung von {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) verwaltet wird, gehört zu einer Ressourcengruppe innerhalb Ihres Kontos. Sie weisen Ressourcen einer Ressourcengruppe zu, während Sie sie auf Basis des Katalogs erstellen. Anschließend können Sie die Nutzung pro Ressourcengruppe in Ihrem Konto anzeigen und Benutzern auf einfache Weise den Zugriff auf alle Ressourcen einer Ressourcengruppe oder auf einzelne Ressourcen in einer Ressourcengruppe erteilen.

Weitere Informationen zum Erstellen von und Arbeiten mit Ressourcengruppen finden Sie im Abschnitt zum [Verwalten von Ressourcengruppen](/docs/resources/resourcegroups.html#rgs).  

## Warum sollte ich meine Cloud Foundry-Serviceinstanzen auf eine Ressourcengruppe migrieren?
{: #instance-migrated}

Durch die Migration Ihrer Cloud Foundry-Services auf eine Ressourcengruppe stehen die von Ihnen benutzten Services für den Einsatz mit der IAM-Zugriffssteuerung und den entsprechenden Ressourcengruppen zur Verfügung. Sie können die differenzierte Zugriffssteuerung mithilfe von IAM-Rollen nutzen. Außerdem können Sie die Informationen zur Nutzung pro Ressourcengruppe in Ihrem Konto anzeigen. 

Wenn Sie über Cloud Foundry-Services verfügen, die in eine Ressourcengruppe migriert werden können, erhalten Sie eine Benachrichtigung in Ihrem Dashboard. Weitere Informationen zum Migrationsprozess finden Sie im Abschnitt zum [Migrieren von Cloud Foundry-Serviceinstanzen und -Apps in eine Ressourcengruppe](/docs/resources/instance_migration.html#migrate).

## Warum kann ich keine Ressource erstellen und sie zu einer Ressourcengruppe hinzufügen?
{: #create-add-resource}

Mit hoher Wahrscheinlichkeit liegt auf Ihrem System ein Problem mit dem Zugriff vor. Sie müssen mindestens über die Rolle eines Anzeigeberechtigten für die Ressourcengruppe selbst und mindestens über die Rolle eines Bearbeiters für den Service im Konto verfügen. Sie können sich an den zuständigen Kontoadministrator wenden, um Ihren zugewiesenen Zugriff im Konto überprüfen zu lassen. 

## Wer kann Ressourcengruppen erstellen?
{: #create-resource}

Sie können Ressourcengruppen nur dann erstellen, wenn Ihnen die Administratorrolle für alle IAM-fähigen {{site.data.keyword.Bluemix_notm}}-Services im Konto zugewiesen wurde.

## Kann ich eine Ressourcengruppe löschen?
{: #delete-resource-group}

Nach der Erstellung können Sie eine Ressourcengruppe nicht mehr löschen.

## Kann ich Serviceinstanzen von einer Ressourcengruppe in eine andere Ressourcengruppe verschieben?
{: #instances-between-rgs}

Die Verschiebung von Serviceinstanzen von einer Ressourcengruppe in eine andere Ressourcengruppe ist nicht möglich. Wenn Ihnen bei der Zuweisung einer Serviceinstanz ein Fehler unterlaufen ist, dann müssen Sie die Instanz löschen und erneut erstellen, um sie der korrekten Ressourcengruppe zuzuweisen.  

## Kann ich Informationen zur Nutzung pro Ressourcengruppe anzeigen?
{: #view-usage}

Ja, das können Sie. Um die Seite 'Nutzungsdashboard' zu öffnen, klicken Sie auf **Verwalten > Abrechnung und Nutzung > Nutzung**. Sie können für das Konto eine Zusammenfassung zur Nutzung nach Ressourcengruppen anzeigen. 
