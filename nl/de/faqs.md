---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-07"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Häufig gestellte Fragen (FAQs)
{: #resources-faq}

## Was ist eine Ressourcengruppe?
{: #resource-group}
{: faq}

Eine Ressourcengruppe bietet Ihnen die Möglichkeit, Ihre Kontoressourcen in anpassbaren Gruppierungen zu organisieren. Jede Kontoressource, die mit der Zugriffssteuerung von {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) verwaltet wird, gehört zu einer Ressourcengruppe innerhalb Ihres Kontos. Sie weisen Ressourcen einer Ressourcengruppe zu, während Sie sie auf Basis des Katalogs erstellen. Anschließend können Sie die Nutzung pro Ressourcengruppe in Ihrem Konto anzeigen und Benutzern auf einfache Weise den Zugriff auf alle Ressourcen einer Ressourcengruppe oder auf einzelne Ressourcen in einer Ressourcengruppe erteilen.

Weitere Informationen zum Erstellen von und Arbeiten mit Ressourcengruppen finden Sie im Abschnitt zum [Verwalten von Ressourcengruppen](/docs/resources/resourcegroups.html#rgs).  

## Warum sollte ich meine Cloud Foundry-Serviceinstanzen auf eine Ressourcengruppe migrieren?
{: #instance-migrated}
{: faq}

Durch die Migration Ihrer Cloud Foundry-Services auf eine Ressourcengruppe stehen die von Ihnen benutzten Services für den Einsatz mit der IAM-Zugriffssteuerung und den entsprechenden Ressourcengruppen zur Verfügung. Sie können die differenzierte Zugriffssteuerung mithilfe von IAM-Rollen nutzen. Außerdem können Sie die Informationen zur Nutzung pro Ressourcengruppe in Ihrem Konto anzeigen. 

Wenn Sie über Cloud Foundry-Services verfügen, die in eine Ressourcengruppe migriert werden können, erhalten Sie eine Benachrichtigung in Ihrer Ressourcenliste. Weitere Informationen zum Migrationsprozess finden Sie im Abschnitt zum [Migrieren von Cloud Foundry-Serviceinstanzen und -Apps in eine Ressourcengruppe](/docs/resources/instance_migration.html#migrate).

## Warum kann ich keine Ressource erstellen und sie zu einer Ressourcengruppe hinzufügen?
{: #create-add-resource}
{: faq}

Mit hoher Wahrscheinlichkeit liegt auf Ihrem System ein Problem mit dem Zugriff vor. Sie müssen mindestens über die Rolle eines Anzeigeberechtigten für die Ressourcengruppe selbst und mindestens über die Rolle eines Bearbeiters für den Service im Konto verfügen. Weitere Informationen finden Sie unter [Ressourcen zu einer Ressourcengruppe hinzufügen](/docs/resources/resourcegroups.html#adding-resources-to-a-resource-group).

Weitere Informationen zum Überprüfen des zugeordneten Zugriffs finden Sie unter [Zugeordneten Zugriff prüfen](/docs/iam/mngiam.html#reviewing-your-assigned-access).

Wenn Sie zusätzlichen Zugriff auf das Konto benötigen, setzen Sie sich mit dem Kontoeigner in Verbindung, der auf der Seite [Benutzer](https://{DomainName}/iam#/users) aufgelistet ist. 

## Wer kann Ressourcengruppen erstellen?
{: #create-resource}
{: faq}

Sie können Ressourcengruppen nur dann erstellen, wenn Ihnen die Administratorrolle für alle IAM-fähigen {{site.data.keyword.Bluemix_notm}}-Services im Konto zugewiesen wurde.

## Kann ich eine Ressourcengruppe löschen?
{: #delete-resource-group}
{: faq}

Nach der Erstellung können Sie eine Ressourcengruppe nicht mehr löschen.

## Kann ich Serviceinstanzen von einer Ressourcengruppe in eine andere Ressourcengruppe verschieben?
{: #instances-between-rgs}
{: faq}

Die Verschiebung von Serviceinstanzen von einer Ressourcengruppe in eine andere Ressourcengruppe ist nicht möglich. Wenn Ihnen bei der Zuweisung einer Serviceinstanz ein Fehler unterlaufen ist, müssen Sie die Instanz löschen und erneut erstellen, um sie der korrekten Ressourcengruppe zuzuweisen.  

## Kann ich Informationen zur Nutzung pro Ressourcengruppe anzeigen?
{: #view-usage}
{: faq}

Ja, das können Sie. Klicken Sie zum Öffnen der Dashboardseite 'Nutzung' auf **Verwalten** &gt; **Abrechnung und Nutzung**. Wählen Sie **Nutzung** aus, um eine Nutzungsübersicht für die einzelnen Ressourcengruppen für das Konto anzuzeigen. 
