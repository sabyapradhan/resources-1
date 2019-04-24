---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Benutzern Zugriff zum Hinzufügen und Entfernen von Ressourcentags erteilen
{: #access}

Als Kontoeigner können Sie einen Teil der Zuständigkeit für das Ressourcentagging delegieren. Erteilen Sie dazu anderen Benutzern des Kontos den erforderlichen Zugriff für das Hinzufügen und Entfernen von Ressourcentags. Benutzer des Kontos können Tags zu einer Ressource hinzufügen, wenn ihnen die erforderliche Zugriffsberechtigung zugewiesen wurde. Der Zugriff auf Services, die zu einer Ressourcengruppe gehören, wird über IAM-Zugriffsrichtlinien von {{site.data.keyword.Bluemix}} (IAM = Identity and Access Management, Identitäts- und Zugriffsmanagement) gesteuert, der Zugriff auf Services, die zu einer Cloud Foundry-Organisation und einem Cloud Foundry-Bereich gehören, über Rollen für Cloud Foundry-Organisationen und -Bereiche.
{: shortdesc}

## Tagberechtigungen
{: #tagging-permissions}

Tags sind für alle Benutzer in einem Konto sichtbar. Sobald eine Ressource mit einem Tag versehen ist, ist der Tag für alle Benutzer sichtbar, die über einen Lesezugriff auf die Ressource verfügen. Zum Hinzufügen oder Entfernen eines Ressourcentags sind je nach Ressourcentyp bestimmte Zugriffsrollen bzw. Zugriffsberechtigungen erforderlich. Entnehmen Sie der folgenden Tabelle die Rollen, die für die einzelnen Ressourcentypen erforderlich sind.


| Ressourcentyp | Rolle |
|--------|---------------|
| IAM-fähig | Bearbeiter- oder Administratorrolle für die Ressource |
| Cloud Foundry | Entwicklerrolle für den Bereich, zu dem die Ressource gehört  |
| Klassische Infrastruktur*| Berechtigung zum Anzeigen von Hardwaredetails oder Berechtigung zum Anzeigen von Details virtueller Server |
| Cloud Object Storage S3 für klassische Infrastruktur | Berechtigung zum Verwalten von Speicher |
{: caption="Tabelle 1. Für das Hinzufügen und Entfernen von Tags erforderliche Rollen" caption-side="top"}

*In der klassischen Infrastruktur können den folgenden Ressourcen Tags hinzugefügt werden: virtuelle Gastmaschine, virtueller dedizierter Host, Network Application Delivery Controller, Gateway-Member, Teilnetz, VLAN und VLAN-Firewall (dediziert).


## Taggingzugriff für IAM-fähige Ressourcen erteilen
{: #iam-managed}

Ressourcen, die zu einer Ressourcengruppe gehören, werden über IAM-Richtlinien von {{site.data.keyword.Bluemix_notm}} verwaltet. Weisen Sie einem Benutzer wie folgt die Bearbeiterrolle (Editorrolle) für das Hinzufügen und Entfernen von Tags zu IAM-fähigen Ressourcen zu:

  1. Klicken Sie in der {{site.data.keyword.Bluemix_notm}}-Konsole auf **Verwalten> Zugriff (IAM)** und wählen Sie **Benutzer** aus.
  2. Klicken Sie auf den Namen des Benutzers, dem Zugriffsberechtigungen erteilt werden sollen.
  3. Klicken Sie auf **Zugriffsrichtlinien** > **Zugriff zuweisen**.
  4. Wählen Sie die Option **Zugriff zu Ressourcen zuweisen** aus.
  5. Wählen Sie in der Serviceliste einen bestimmten Service oder die Option **Alle Services mit aktiviertem Identity and Access Management** aus.
  6. Wählen Sie in der Liste der plattformbezogenen Zugriffsrollen die Rolle**Editor (Bearbeiter)** aus.
  7. Klicken Sie auf **Zuweisen**.

## Zugriff für das Tagging von Cloud Foundry-Ressourcen erteilen
{: #cf_tag_access}

Ressourcen, die zu einer Cloud Foundry-Organisation oder einem Cloud Foundry-Bereich gehören, werden über Cloud Foundry-Organisationsrollen und -Bereichsrollen verwaltet. Weisen Sie einem Benutzer wie folgt die Bereichsrolle 'Entwickler' für das Hinzufügen und Entfernen von Tags zu CLoud Foundry-Ressourcen zu:

 1. Klicken Sie auf **Verwalten > Zugriff (IAM)** und wählen Sie **Benutzer** aus.
2. Wählen Sie den Namen des Benutzers aus, dem Zugriffsberechtigungen erteilt werden sollen.
3. Klicken Sie auf **Cloud Foundry-Zugriff**.
4. Klicken Sie auf **Organisation zuweisen**.
5. Erweitern Sie den Eintrag `Organisation` und wählen Sie die Organisation mit der Serviceinstanz aus, für die dem Benutzer Zugriff erteilt werden soll.
6. Wählen Sie die Region aus.
7. Wählen Sie die Bereichsrolle **Entwickler** aus.
8. Klicken Sie auf **Rolle speichern**.

## Zugriff für das Tagging von Ressourcen der klassischen Infrastruktur erteilen
{: #classic-infra}

Weisen Sie einem Benutzer wie folgt die Servicezugriffsrolle 'Manager' für das Hinzufügen und Entfernen von Tags zu Services der klassischen Infrastruktur zu.

  1. Klicken Sie auf **Verwalten > Zugriff (IAM)** und wählen Sie **Benutzer** aus.
  2. Klicken Sie auf den Namen des Benutzers, dem Zugriffsberechtigungen erteilt werden sollen.
  3. Klicken Sie auf **Klassische Infrastruktur**.
  4. Erweitern Sie auf der Registerkarte **Berechtigungen** die Kategorie **Einheiten**.
  5. Wählen Sie **Hardwaredetails anzeigen** und **Details zu virtuellen Servern anzeigen** aus. Wenn Zugriff für Cloud Object Storage S3 erteilt werden soll, weisen Sie die Berechtigung für das Verwalten von Speicher**** zu.
  6. Klicken Sie auf **Speichern**.
  7. Klicken Sie auf die Registerkarte **Einheiten**.
  8. Wählen Sie je nach der Ressource, der Tags hinzugefügt werden sollen, **Alle Bare-Metal-Server** oder **Alle virtuellen Server ** aus.
