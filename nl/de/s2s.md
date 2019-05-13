---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-06"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Services mit einer Cloud Foundry-App verbinden
{: #s2s_binding}

Um einen Service in einer Cloud Foundry-App zu verwenden, müssen Sie eine Verbindung erstellen oder diesen Service an die App binden.
{: shortdesc}

Führen Sie die folgenden Schritte aus, um einen Service an Ihre App zu binden, indem Sie auf der Detailseite für einen bestimmten Service starten:

Sie können auch Verbindungen aus Ihrer App mit dem Service erstellen. Wählen Sie Ihre App in der Ressourcenliste aus, gehen Sie zum Menü **Verbindungen** und wählen Sie den Service aus.
{: note}

1. Klicken Sie in der Ressourcenliste auf **Services** und wählen Sie den Service aus, auf den zugegriffen werden soll. Die Detailseite für den Service wird angezeigt.
2. Klicken Sie in der Navigation auf **Verbindungen**.
3. Klicken Sie auf **Verbindung erstellen**.
4. Klicken Sie in der Zeile der App, für die Sie die Verbindung erstellen möchten, auf **Verbinden**.
5. Wählen Sie eine Zugriffsrolle aus, um die Verbindung zuzuweisen. Diese Rolle definiert die zulässigen Aktionen, die von der App, die auf den Service zugreift, ausgeführt werden können.
6. Optional: Wählen Sie eine Service-ID für die App aus, erstellen Sie eine oder lassen Sie automatisch eine generieren, um damit auf den Service zuzugreifen. Dieser Service-ID wird die Zugriffsrolle zugewiesen, die Sie im vorherigen Schritt ausgewählt haben. Falls Sie keine Option auswählen, wird eine ID generiert.
7. Optional: Fügen Sie Konfigurationsparameter im JSON-Format hinzu.
8. Klicken Sie auf **Verbindung herstellen & erneutes Staging für App ausführen**.


Wenn Sie den Zugriff von Apps auf die Serviceinstanz einschränken möchten, klicken Sie im Navigationsbereich auf **Verbindungen** und entfernen Sie die Servicebindung anschließend mithilfe von **Bindung aufheben**.
{: tip}
