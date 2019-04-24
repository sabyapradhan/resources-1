---

copyright:

  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service key, api key, bind, credential

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}


# Berechtigungsnachweis hinzufügen
{: #service_credentials}

Sie können eine neue Gruppe von Berechtigungsnachweisen für die Fälle generieren, in denen Sie einen externen Konsumenten manuell mit einem {{site.data.keyword.Bluemix}}-Service verbinden möchten. Wenn Sie beispielsweise versuchen, eine AWS-App an einen Watson-Service zu binden, müssen Sie einen neuen Berechtigungsnachweis generieren, der für das Binden von App und Service verwendet werden kann.

## Berechtigungsnachweis beim Binden eines IAM-fähigen Service hinzufügen
{: #IAM}

Services, die von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) verwaltet werden, können einen Ressourcenschlüssel generieren, der auch als Berechtigungsnachweis bezeichnet wird. Berechtigungsnachweise sind servicespezifisch und variieren abhängig davon, wie der jeweilige Service die Berechtigungsnachweise definiert, die generiert werden müssen. Ein Berechtigungsnachweis kann zum Beispiel einen Benutzernamen, ein Kennwort, einen Hostnamen, einen Port und eine URL enthalten.

Während der Inhalt des jeweiligen Berechtigungsnachweises für den Service, der ihn generiert, eindeutig ist, setzen alle Services, die von IAM verwaltet werden, voraus, dass neue Berechtigungsnachweise eine Zugriffsrolle für den IAM-Service enthalten. Einige Services generieren möglicherweise zusätzliche Daten, für die die Angabe von Parametern erforderlich ist. So kann es bei einem Service zum Beispiel erforderlich sein, einen Sprachparameter einzugeben, mit dem die Standardsprache festgelegt wird, die im generierten Ressourcenschlüssel zurückgegeben wird.

Führen Sie die folgenden Schritte aus, um einen Berechtigungsnachweis für einen von IBM verwalteten Service hinzuzufügen:

1. Wählen Sie in der Ressourcenliste den Namen des Service aus, um die Seite mit den Servicedetails zu öffnen. Wählen Sie dann die Registerkarte für Berechtigungsnachweise aus und klicken Sie auf **Neuen Berechtigungsnachweis + **.
2. Geben Sie im Dialogfeld für das Hinzufügen eines neuen Berechtigungsnachweises einen **Name** an.
3. Geben Sie die Rolle an. Dieser Wert legt die Zugriffsrolle des IAM-Service fest. Weitere Informationen finden Sie unter [IAM-Zugriff](/docs/iam?topic=iam-userroles)
4. Optional können Sie eine Service-ID bereitstellen, indem Sie IAM einen eindeutigen Wert für Sie generieren lassen oder indem Sie eine vorhandene Service-ID bereitstellen. Weitre Informationen finden Sie in [Service-IDs erstellen und verwenden](/docs/iam?topic=iam-serviceids).
5. Optional können Sie weitere Parameter als gültiges JSON-Objekt mit servicespezifischen Konfigurationsparametern inline oder in einer Datei angeben.

  Für die meisten Services sind keine zusätzlichen Parameter erforderlich. Bei den Services, die zusätzliche Parameter erfordern, definiert jeder Service eine eigene Parameterliste. Eine Liste der unterstützten Konfigurationsparameter finden Sie in der Dokumentation für das jeweilige Serviceangebot.
  {: note}
6. Klicken Sie auf **Hinzufügen**, um den neuen Serviceberechtigungsnachweis zu generieren.

## Berechtigungsnachweis beim Binden eines Cloud Foundry-Service hinzufügen
{: #cf_credential}

Cloud Foundry-Services können einen Serviceschlüssel - auch als Berechtigungsnachweis bezeichnet - generieren. Berechtigungsnachweise sind servicespezifisch und variieren abhängig davon, wie der jeweilige Service die Berechtigungsnachweise definiert, die generiert werden müssen. Ein Serviceberechtigungsnachweis kann zum Beispiel einen Benutzernamen, ein Kennwort, einen Hostnamen, einen Port und eine URL enthalten.

Der Inhalt des jeweiligen Berechtigungsnachweises ist jedoch für den Service, der ihn generiert, eindeutig. Einige Services generieren möglicherweise zusätzliche Daten, für die die Angabe von Parametern erforderlich ist. So kann es bei einem Service zum Beispiel erforderlich sein, einen Sprachparameter einzugeben, mit dem die Standardsprache festgelegt wird, die im generierten Serviceschlüssel zurückgegeben wird.

Führen Sie die folgenden Schritte aus, um einen Cloud Foundry-Berechtigungsnachweis hinzuzufügen:

1. Wählen Sie auf der Servicedetailseite die Registerkarte mit den Berechtigungsnachweisen aus und klicken Sie auf **Neuen Berechtigungsnachweis + **.
2. Geben Sie im Dialogfeld für das Hinzufügen eines neuen Berechtigungsnachweises einen **Name** an.
3. Optional können Sie weitere Parameter als gültiges JSON-Objekt mit servicespezifischen Konfigurationsparametern inline oder in einer Datei angeben.

  Für die meisten Services sind keine zusätzlichen Parameter erforderlich. Bei den Services, die zusätzliche Parameter erfordern, definiert jeder Service eine eigene Parameterliste. Eine Liste der unterstützten Konfigurationsparameter finden Sie in der Dokumentation für das jeweilige Serviceangebot.
  {: note}
4. Klicken Sie auf **Hinzufügen**, um den neuen Serviceberechtigungsnachweis zu generieren.
