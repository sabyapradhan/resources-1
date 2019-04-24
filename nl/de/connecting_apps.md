---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: create connection, connect a service, bind, alias

subcollection: resources

---

{:shortdesc: .shortdesc}

# Verbindungen verwalten
{: #connect_app}

Sie können einen Service über die Registerkarte **Verbindungen** in Ihrem Service-Dashboard mit einer vorhandenen oder neuen {{site.data.keyword.Bluemix}}-Anwendung verbinden. Wenn Sie einen Service mit einer Anwendung verbinden, entsteht eine Bindung zwischen Service und Anwendung. Über die Registerkarte **Verbindungen** können Sie diese Bindung aufheben, weitere Verbindungen hinzufügen oder Verbindungen löschen.

Wenn Sie jedoch eine Serviceinstanz, die von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) verwaltet wird, mit einer Anwendung verbinden, so wird ein Aliasname des Service, der von IAM verwaltet wird, in dem entsprechenden Bereich mit den von Ihnen angegebenen Bindungsinformationen erstellt. Dieser Aliasname wird als Serviceinstanz Ihres IAM-verwalteten Service dargestellt.
{:shortdesc}

## Was ist ein Aliasname?
{: #what_is_alias}

Ein Aliasname ist eine Verbindung zwischen Ihrem IAM-verwalteten Service in einer Ressourcengruppe und einer Anwendung in einer Organisation oder einem Bereich. In der {{site.data.keyword.Bluemix_notm}}-Konsole wird die Verbindung (Aliasname) als Serviceinstanz dargestellt. Sie können Ihren Aliasnamen verwalten, indem Sie die Serviceinstanz ändern, die Ihre Verbindung darstellt.

Aliasnamen sind wie symbolische Verbindungen (Symlinks), die Verweise auf ferne Ressourcen enthalten und die Interoperabilität und die Wiederverwendung einer Instanz auf der gesamten Plattform ermöglichen. Sie können beispielsweise eine Instanz eines Service in einer Ressourcengruppe erstellen und sie anschließend aus allen verfügbaren Regionen wiederverwenden, indem Sie einen Aliasnamen in einer Organisation oder einem Bereich in diesen Regionen erstellen.

Die folgenden Regeln gelten für Aliasnamen:

* Es wird keine zusätzliche Gebühr für einen Aliasnamen erhoben, aber jeder Aliasname wird auf das Kontingent in Ihrer Organisation angerechnet.
* In der {{site.data.keyword.Bluemix_notm}}-Konsole können Sie pro Bereich nur einen Aliasnamen erstellen. Mit der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle kann jedoch mehr als ein Aliasname pro Bereich erstellt werden. Weitere Informationen finden Sie in [Mit Ressourcen und Ressourcengruppen arbeiten](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).
* Sie können mehrere Verbindungen zwischen Ihrem IAM-verwalteten Service und einer beliebigen Anwendung in einem Bereich, einer Organisation und einer Region in demselben Konto erstellen, sofern Sie dazu berechtigt sind.
* Mehrere Verbindungen, die in demselben Bereich zu verschiedenen Anwendungen von einer IAM-verwalteten Serviceinstanz hergestellt wurden, verwenden denselben Aliasnamen.
* Wenn Sie die Bindung einer IAM-verwalteten Serviceinstanz aufheben, wird die Serviceinstanz, die den Aliasnamen darstellt, *nicht* gelöscht.
* Wenn Sie die Anwendung löschen, mit der Ihre IAM-verwaltete Serviceinstanz verbunden ist, wird die Instanz, die den Aliasnamen darstellt, *nicht* gelöscht.
* Wenn Sie eine IAM-verwaltete Serviceinstanz löschen, wird die Serviceinstanz, die den Aliasnamen darstellt, *gelöscht*.

## Verbindung (Aliasname) zwischen einem IAM-verwalteten Service und einer App herstellen
{: #creating_alias}

Gehen Sie wie folgt vor, um Ihre IAM-verwaltete Serviceinstanz mit einer Anwendung zu verbinden:

1. Rufen Sie Ihr Dashboard auf.

2. Klicken Sie auf den Namen Ihrer App, um die App-Detailansicht zu öffnen.

3. Klicken Sie auf **Vorhandenen verbinden** und treffen Sie bei Ihrer vorhandenen App eine Auswahl. Wahlweise können Sie auf **Verbindung erstellen** klicken, um eine App zu erstellen, zu der eine Verbindung hergestellt werden soll.

4. Geben Sie die **Zugriffsrolle für Verbindung** an. Dieser Wert legt die Zugriffsrolle des IAM-Service fest. Weitere Informationen finden Sie unter [IAM-Zugriff](/docs/iam?topic=iam-userroles).

5. Optional können Sie eine **Service-ID für Verbindung** bereitstellen, indem Sie IAM einen eindeutigen Wert generieren lassen oder indem Sie eine vorhandene Service-ID bereitstellen. Weitere Informationen finden Sie in [Service-IDs erstellen und verwenden](/docs/iam?topic=iam-serviceids).

6. Klicken Sie auf **Erstellen**.

## Aliasnamen anzeigen
{: #view_alias}

Nachdem Sie eine Verbindung zwischen einem IAM-verwalteten Service und einer App erstellt haben, wird der Aliasname auf der Registerkarte **Verbindungen** der verbundenen App angezeigt. Darüber hinaus wird der Aliasname als aktive Serviceinstanz in Ihrer Ressourcenliste angezeigt und enthält nur dann eine Registerkarte **Verbindungen**, wenn Sie den Alias öffnen.

1. Rufen Sie Ihre Ressourcenliste auf.
2. Klicken Sie in der Tabelle **Application Services** auf den Namen der Serviceinstanz, um die Ansicht mit den Servicedetails zu öffnen. Wenn nur eine Registerkarte **Verbindungen** enthalten ist, handelt es sich um einen Aliasnamen.

## Aliasnamen löschen
{: #delete_alias}

Am einfachsten lässt sich der Aliasname löschen, indem Sie die IAM-verwaltete Serviceinstanz löschen. Sie können Ihre IAM-verwaltete Serviceinstanz aber auch beibehalten und den Aliasnamen direkt löschen.

1. Rufen Sie Ihre Ressourcenliste auf.
2. Klicken Sie in der Tabelle **Application Services** auf den Namen der Serviceinstanz, um die Ansicht mit den Servicedetails zu öffnen. Wenn nur eine Registerkarte **Verbindungen** enthalten ist, handelt es sich um einen Aliasnamen.
3. Löschen Sie die Instanz.

## Verbindung zwischen mehreren Services erstellen
{: #multiple_services}

Weitere Informationen finden Sie in [Services in einem anderen Service verwenden](/docs/resources?topic=resources-s2s_binding).
