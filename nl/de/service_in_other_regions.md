---

copyright:
  years: 2015, 2018
lastupdated: "2018-06-14"

---

{:shortdesc: .shortdesc}

# Services in einer anderen Region verwenden
{: #cross_region_service}

Wenn Sie über eine Serviceinstanz verfügen, die erstellt und an Apps in einer einzigen Region gebunden wurde, können Sie diese Serviceinstanz mit einer der folgenden Methoden in einer anderen Region verwenden:
{: shortdesc}

  * Verwenden Sie die Serviceberechtigungsnachweise, um Ihre App-Instanz direkt zu konfigurieren. Details finden Sie unter [Externen Apps die Verwendung von {{site.data.keyword.Bluemix_notm}}-Services ermöglichen](/docs/apps/reqnsi.html#accser_external){: new_window}.
  * Erstellen Sie einen vom Benutzer bereitgestellten Service als Bridge.

	Führen Sie die folgenden Schritte aus, um eine Serviceinstanz zu verwenden, die in einer anderen Region existiert:

      1. Wechseln Sie in die Region, in der die Serviceinstanz existiert. Erweitern Sie im Dashboard der {{site.data.keyword.Bluemix_notm}}-Konsole das Menü **Standort** und wählen Sie die Region aus, in der sich die Serviceinstanz befindet.

      2. Rufen Sie die Berechtigungsnachweise und Verbindungsparameter aus der Umgebungsvariablen VCAP_SERVICES der Serviceinstanz in der Region ab, in der sich der Service befindet. Führen Sie die folgenden Schritte aus:

	       1. Klicken Sie im {{site.data.keyword.Bluemix_notm}}-Dashboard auf die Anwendungskachel. Die Übersichtsseite wird angezeigt.
	       2. Klicken Sie im Navigationsbereich auf **Berechtigungsnachweise**. Die Details zur Umgebungsvariablen *VCAP_SERVICES* werden angezeigt. Dokumentieren Sie den JSON-Inhalt für die Serviceinstanz.

      3. Wechseln Sie zu der Region, in der Sie die Serviceinstanz verwenden möchten. Erweitern Sie im Dashboard der {{site.data.keyword.Bluemix_notm}}-Konsole das Menü **Standort** und wählen Sie die Region aus, in der Sie die Serviceinstanz verwenden möchten.

      4. Erstellen Sie eine vom Benutzer zur Verfügung gestellte Serviceinstanz, indem Sie die Berechtigungsnachweise und Verbindungsparameter verwenden, die Sie aus der Umgebungsvariablen *VCAP_SERVICES* aufgezeichnet haben. Weitere Informationen finden Sie in [Vom Benutzer bereitgestellte Serviceinstanz erstellen](/docs/apps/reqnsi.html#user_provide_services).

      5. Binden Sie die vom Benutzer bereitgestellte Serviceinstanz mit dem folgenden Befehl an Ihre App:

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
