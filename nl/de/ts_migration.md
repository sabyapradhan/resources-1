---

copyright:

  years: 2018

lastupdated: "2018-06-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Fehlerbehebung für die Migration von Serviceinstanzen

Wenn bei der Migration einer Cloud Foundry-Serviceinstanz zu einer Ressourcengruppe Fehler auftreten, prüfen Sie die folgenden gängigen Probleme auf Informationen, die Ihnen dabei helfen, die Migration fortzusetzen.

## Eine Serviceinstanz wurde zur falschen Ressourcengruppe migriert

Sie können Ressourcen nicht zwischen Ressourcengruppen verschieben, nachdem sie zugewiesen wurden. Wenn Sie also eine Instanz der falschen Ressourcengruppe zugewiesen haben, können Sie versuchen, die Instanz zu löschen und eine neue aus dem Katalog zu erstellen. Sie können sie der richtigen Ressourcengruppe zuweisen, wenn Sie die Instanz erstellen.

## Ein Benutzer in dem Konto kann eine berechtigte Instanz nicht migrieren

Möglicherweise verfügen Sie nicht über die erforderliche Zugriffsrechte für das Migrieren einer Serviceinstanz. Weitere Informationen finden Sie unter [Wer kann Serviceinstanzen migrieren?](/docs/resources/instance_migration.html#whocanmigrate) 

## Nicht alle Services sind für die Migration berechtigt

Derzeit können nicht alle Services zu Ressourcengruppen hinzugefügt und mithilfe von IAM-Zugriffssteuerung und -Ressourcengruppen verwaltet werden. Sie werden benachrichtigt, wenn Services berechtigt werden, falls Sie über die entsprechenden Zugriffsberechtigungen zum Abschließen der Migrationstask verfügen. 
