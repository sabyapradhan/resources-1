---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Fehlerbehebung für die Migration von Serviceinstanzen

Wenn bei der Migration einer Cloud Foundry-Serviceinstanz zu einer Ressourcengruppe Fehler auftreten, prüfen Sie die folgenden gängigen Probleme auf Informationen, die Ihnen dabei helfen, die Migration fortzusetzen.

## Was passiert, wenn ich meine Serviceinstanz in die falsche Ressourcengruppe migriert habe?

Derzeit können Sie Ressourcen nicht zwischen Ressourcengruppen verschieben, nachdem sie zugewiesen wurden. Wenn Sie also eine Instanz in die falsche Ressourcengruppe migriert haben, können Sie versuchen, die Instanz zu löschen und eine neue aus dem Katalog zu erstellen. Sie können sie der richtigen Ressourcengruppe zuweisen, wenn Sie die Instanz erstellen.

## Warum kann ich nicht migrieren?

Möglicherweise verfügen Sie nicht über die erforderliche Zugriffsrechte für das Migrieren einer Serviceinstanz. Weitere Informationen finden Sie unter [Wer kann Serviceinstanzen migrieren?](/docs/account/instance_migration.html#whocanmigrate)

## Warum kommen nicht alle meine Services für die Migration infrage?

Derzeit sind nicht alle Services für die Verwaltung mithilfe von IAM-Zugriffssteuerung und -Ressourcengruppen verfügbar. Sie werden benachrichtigt, wenn Services die Verwendung von IAM zulassen, falls Sie über die entsprechenden Zugriffsberechtigungen zum Abschließen der Migrationstask verfügen.
