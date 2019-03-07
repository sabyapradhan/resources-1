---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# Services in einer anderen Region verwenden
{: #cross_region_service}

Wenn Sie über eine Serviceinstanz verfügen, die erstellt und an Apps in einer einzigen Region gebunden wurde, können Sie diese Serviceinstanz mit einer der folgenden Methoden in einer anderen Region verwenden:
{: shortdesc}

  * Verwenden Sie die Serviceberechtigungsnachweise, um Ihre App-Instanz direkt zu konfigurieren. Ausführliche Informationen finden Sie in [Verbindung von Services zu externen Apps herstellen](/docs/resources?topic=resources-externalapp#externalapp).
  * Erstellen Sie einen vom Benutzer bereitgestellten Service als Bridge.

	Führen Sie die folgenden Schritte aus, um eine Serviceinstanz zu verwenden, die in einer anderen Region existiert:

      1. Klicken Sie zum Wechsel in die Region mit der Serviceinstanz auf das **Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg)** und danach auf **Ressourcenliste**. Erweitern Sie anschließend das Menü **Standort** und wählen Sie die Region aus.

      2. Rufen Sie die Berechtigungsnachweise und Verbindungsparameter aus der Umgebungsvariablen VCAP_SERVICES der Serviceinstanz in der Region mit dem Service ab. Führen Sie die folgenden Schritte aus:

	       1. Klicken Sie im {{site.data.keyword.Bluemix_notm}}-Dashboard in der Anwendungskachel auf **Alles anzeigen**. Die Übersichtsseite wird angezeigt.
	       2. Klicken Sie im Navigationsbereich auf **Berechtigungsnachweise**. Die Details zur Umgebungsvariablen *VCAP_SERVICES* werden angezeigt. Dokumentieren Sie den JSON-Inhalt für die Serviceinstanz.

      3. Wechseln Sie zu der Region, in der Sie die Serviceinstanz verwenden möchten. Klicken Sie auf das **Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg)** und danach auf **Ressourcenliste**. Erweitern Sie anschließend das Menü **Standort** und wählen Sie die Region aus, in der Sie die Serviceinstanz verwenden möchten.

      4. Erstellen Sie eine vom Benutzer zur Verfügung gestellte Serviceinstanz, indem Sie die Berechtigungsnachweise und Verbindungsparameter verwenden, die Sie aus der Umgebungsvariablen *VCAP_SERVICES* aufgezeichnet haben.

      5. Binden Sie die vom Benutzer bereitgestellte Serviceinstanz mit dem folgenden Befehl an Ihre App:

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
