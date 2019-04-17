---

copyright:

  years: 2018, 2019
lastupdated: "2019-04-03"

keywords: add tags, tags, full list of tags, how to use tags

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Mit Tags arbeiten
{: #tag}

Bei Tags handelt es sich um Bezeichnungen, die Sie Ressourcen zuordnen, um das Filtern von Ressourcen in der Ressourcenliste zu erleichtern. Mit Tags können Sie Ihre Ressourcen strukturieren und sie anschließend leichter finden. Beim Anzeigen Ihres [exportierten Nutzungsberichts](/docs/billing-usage?topic=billing-usage-viewingusage#export-csv) können Sie auch Tags verwenden, um die Nutzung durch bestimmte Teams oder die Kostenzuordnung leichter zu erkennen.
{: shortdesc}

Rufen Sie **Verwalten > Konto** auf und wählen Sie **Tags** aus, um eine vollständige Liste der Tags in Ihrem Konto anzuzeigen.

## Tagregeln und -einschränkungen
{: #limits}

Die maximale Größe eines Tags beträgt 128 Zeichen. Zulässige Zeichen sind A-Z, 0-9, Leerraum, Unterstreichungszeichen, Bindestrich, Punkt und Doppelpunkt. Bei Tags wird die Groß-/Kleinschreibung nicht beachtet. Durch Doppelpunkte wird der Tag zu einer Zeichenfolge, in der zwei logische Teile isoliert werden wie bei einem `Schlüssel:Wert`-Paar. Es ist nicht möglich, einen Doppelpunkt in einem Tag zu verwenden, ohne dass ein solches Paar erstellt wird. Kommas werden zum Trennen von Tags verwendet und dürfen deshalb nicht im Tagnamen verwendet werden.

## Tags zu einer Ressource hinzufügen und entfernen
{: #add-remove}

1. Klicken Sie in der {{site.data.keyword.Bluemix_notm}}-Konsole auf das Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) und dann auf **Ressourcenliste**, um Ihre Ressourcenliste anzuzeigen.
2. Erweitern Sie das Pfeilsymbol für den Ressourcentyp, dem die zu taggende Ressource angehört. Erweitern Sie beispielsweise den Eintrag **Speicher**, wenn ein Tag zu einer {{site.data.keyword.cos_full_notm}}-Instanz hinzugefügt werden soll.  
3. Klicken Sie auf das Symbol **Aktionen** ![Aktionssymbol](../icons/action-menu-icon.svg), um ein Tag für die Ressource hinzuzufügen oder zu aktualisieren.

    * Klicken Sie zum Hinzufügen eines Tags auf das Menü **Aktionen** ![Aktionssymbol](../icons/action-menu-icon.svg), wählen Sie **Tags hinzufügen** aus und geben Sie einen Namen für Ihren Tag ein.
    * Klicken Sie zum Hinzufügen weiterer Tags auf das Symbol **Bearbeiten** ![Bearbeitungssymbol](../icons/edit-tagging.svg) neben dem angezeigten Tag und geben Sie einen Namen für Ihren Tag ein. Drücken Sie die Eingabetaste, um weitere Tags hinzuzufügen.
4. Klicken Sie zum Entfernen eines Tags auf das Symbol **Bearbeiten** ![Bearbeitungssymbol](../icons/edit-tagging.svg). Klicken Sie anschließend auf das Symbol **Entfernen** ![Symbol 'Entfernen'](../icons/close-tagging.svg) neben dem Tag.

## Nach Tags suchen
{: #search-tags}

Für die Suche nach Tags stehen Ihnen verschiedene Möglichkeiten zur Auswahl:

  * Verwenden Sie die Suchleiste in der Menüleiste der {{site.data.keyword.Bluemix_notm}}-Konsole.
  * Filtern Sie die Ressourcenliste anhand des gesuchten Tags.
  * Lokalisieren Sie auf der Seite 'Anwendungsdetails' die Tags, die der jeweiligen Ressource zugeordnet sind.

Derselbe Tag kann von verschiedenen Benutzern zu unterschiedlichen Ressourcen in demselben Abrechnungskonto zugeordnet werden und es ist zu beachten, dass nicht alle Ressourcen für alle Benutzer im Konto sichtbar sind.
{: note}


## Tagging für Vertriebspartner
{: #resell}

Tags sind für alle Mitglieder eines Kontos sichtbar. Ist Ihr Konto unterschiedlichen Organisationen zugeordnet (beispielsweise, wenn Sie Vertriebspartner sind), sollten Sie Ihren Kunden empfehlen, in Tags keine Daten zu speichern, wodurch anderen Personen im selben Konto vertrauliche Informationen offengelegt werden könnten.

Geben Sie zum Steuern der Sichtbarkeit von Tags die Tagrichtlinien weiter und weisen Sie Benutzer darauf hin, dass Tags innerhalb des gesamten Kontos sichtbar sind.

Verwenden Sie Codes anstelle von Namen für Kunden und Konten und vermeiden Sie es, sensible Informationen in Tags einzuschließen.
{: tip}
