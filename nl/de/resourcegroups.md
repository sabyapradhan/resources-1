---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# Ressourcengruppen verwalten
{: #rgs}

Ressourcengruppen bieten Ihnen die Möglichkeit, Ihre Kontoressourcen in anpassbaren Gruppierungen zu organisieren, sodass Sie den Benutzern schnell Zugriff auf mehrere Ressourcen gleichzeitig zuordnen können. Jede Kontoressource, die mit der Zugriffssteuerung von {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) verwaltet wird, gehört zu einer Ressourcengruppe innerhalb Ihres Kontos. Cloud Foundry-Services werden Organisationen und Bereichen zugewiesen und können nicht zu einer Ressourcengruppe hinzugefügt werden.

Beginnen Sie mit dem Verwalten Ihrer Ressourcengruppen, indem Sie **Verwalten** &gt; **Konto** aufrufen. Erweitern Sie den Eintrag **Kontoressourcen** und wählen Sie anschließend **Ressourcengruppen** aus. Die angezeigte Seite ermöglicht es Ihnen, Ihre Ressourcengruppen anzuzeigen und neue zu erstellen, Ressourcen hinzuzufügen und umzubenennen sowie den Zugriff zu verwalten. Weitere Informationen zur Arbeit mit Ressourcengruppen finden Sie unter [Bewährte Verfahren für die Organisation von Ressourcen in Ressourcengruppen](/docs/resources?topic=resources-bp_resourcegroups).


## Ressourcengruppe erstellen
{: #create_rgs}

Wenn Sie über ein nutzungsabhängiges Konto oder ein Abonnementkonto verfügen, dann können Sie mehrere Ressourcengruppen erstellen, um auf einfache Weise Kontingente zu verwalten und die Informationen zu Abrechnung und Nutzung für ein Ressourcenset anzuzeigen. Durch die Gruppierung von Ressourcen wird außerdem die gleichzeitige Zuweisung von Zugriffsberechtigungen für mehrere Instanzen an die Benutzer erleichtert. Des Weiteren ist zu beachten, dass Sie eine Ressourcengruppe umbenennen, jedoch keine erstellte Ressourcengruppe löschen können.

Wenn Sie über ein Lite-Konto oder ein 30-Tage-Testkonto verfügen, können Sie zwar keine zusätzlichen Ressourcengruppen erstellen, jedoch die Standardressourcengruppe umbenennen.

Verbindungen zwischen einer Ressourcengruppe und einer Cloud Foundry-Organisation oder einem Cloud Foundry-Bereich sind durch Ihr Kontingent eingeschränkt. Weitere Informationen finden Sie in [Was ist ein Alias?](/docs/resources?topic=resources-connect_app#what_is_alias).
{: note}

1. Rufen Sie **Verwalten** &gt; **Konto** auf. Erweitern Sie den Eintrag **Kontoressourcen** und wählen Sie anschließend **Ressourcengruppen** aus. 
2. Klicken Sie auf **Ressourcengruppe erstellen**.
3. Geben Sie einen Namen für Ihre Ressourcengruppe ein.
4. Klicken Sie auf **Hinzufügen**.

## Ressourcen zu einer Ressourcengruppe hinzufügen
{: #add_to_rgs}

Services, die mit IAM verwaltet werden, gehören nicht zu einer Organisation oder einem Bereich von Cloud Foundry, sondern zu einer Ressourcengruppe. Wenn Sie eine Serviceinstanz für einen dieser Services über den Katalog erstellen, werden Sie aufgefordert, die Instanz einer Ressourcengruppe zuzuweisen. Ihre Ressourcengruppenauswahl bei der Erstellung der Instanz ist endgültig und kann nicht geändert werden.

Damit Benutzer in Ihrem Konto Ressourcen aus dem Katalog erstellen und sie einer Ressourcengruppe zuordnen können, müssen ihnen zwei Zugriffsrichtlinien zugewiesen werden:

* Eine Richtlinie mit Rolle des Anzeigeberechtigten ('A') oder höher für die Ressourcengruppe selbst
* Eine Richtlinie mit Rolle des Bearbeiters oder höher für den Service im Konto

## Ressourcen in Ressourcengruppen anzeigen
{: #view_rg_resources}

Um die Ressourcen, die in einer Ressourcengruppe enthalten sind, auf einfache Weise anzeigen zu können, müssen Sie die Ressourcenliste nach Ressourcengruppen filtern.

## Ressourcengruppe umbenennen
{: #rename_rgs}

Ihre erste Ressourcengruppe wird vom System für Sie erstellt und erhält den Namen `Standard`. Sie können auswählen, ob der Name dieser Gruppe oder anderer Gruppen, die Sie erstellen, aktualisiert werden soll.

1. Rufen Sie **Verwalten** &gt; **Konto** auf. Erweitern Sie den Eintrag **Kontoressourcen** und wählen Sie anschließend **Ressourcengruppen** aus. 
2. Wählen Sie im Menü **Aktionen** ![Symbol für Aktionsliste](../icons/action-menu-icon.svg) die Option **Umbenennen** aus.
3. Geben Sie einen eindeutigen Namen ein und klicken Sie auf **Speichern**.

## Ressourcengruppen und Ressourcen mit der {{site.data.keyword.Bluemix_notm}}-CLI verwalten
{: #rgs_cli}

Von der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle werden mehrere Befehle für das Ressourcenmanagement unterstützt. Weitere Informationen finden Sie in [Mit Ressourcen und Ressourcengruppen arbeiten](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource#ibmcloud_commands_resource).

## Zugriff auf eigene Ressourcengruppen verwalten
{: #rgs_manage_access}

Cloud IAM ermöglicht Ihnen die flexible Bereitstellung eines genau differenzierten Benutzerzugriffs auf die Ressourcen in Ihrem Konto. Sie können Cloud IAM dazu verwenden, Benutzern Richtlinien zuzuweisen, die den Benutzerzugriff auf alle Ressourcen einer Ressourcengruppe, auf einen einzelnen Servicetyp in einer Ressourcengruppe oder auf eine einzelne Serviceinstanz im Konto bereitstellen. Wird Benutzern Zugriff auf Ressourcen in einer Ressourcengruppe erteilt, erhalten die Benutzer dadurch nicht auch die Zugriffsberechtigung zum Verwalten der Ressourcengruppe selbst. Sie können den Zugriff auf die Funktionen zum Anzeigen, Bearbeiten und Verwalten der eigentlichen Ressourcengruppe separat definieren.

Weitere Informationen finden Sie unter [Zugriff auf Ressourcen verwalten](/docs/iam?topic=iam-iammanidaccser).
