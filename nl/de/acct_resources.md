---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Was ist eine Ressource?
{: #resource}

Als Ressourcen werden Elemente bezeichnet, die innerhalb einer [Ressourcengruppe](/docs/resources?topic=resources-rgs) erstellt, verwaltet und gespeichert werden können. Beispiel fü Ressourcen sind Apps, Serviceinstanzen, Container-Cluster, Speicherdatenträger und virtuelle Server. Alle Serviceinstanzen, die bei ihrer Erstellung über den Katalog einer Ressourcengruppe hinzugefügt werden können, werden als Ressourcen bezeichnet und mithilfe der IAM-Zugriffssteuerung verwaltet. Die Services, die die Verwendung von [IAM-Rollen](/docs/iam?topic=iam-userroles#iamusermanrol) für den Zugriff und die Organisation innerhalb einer Ressourcengruppe unterstützen, werden als IAM-fähige Services bezeichnet.

Nicht alle Services unterstützen aktuell die Verwendung von Ressourcengruppen und IAM. Alle Serviceinstanzen, die bei ihrer Erstellung über den Katalog Cloud Foundry-Organisationen und -Bereichen hinzugefügt werden, unterscheiden sich deutlich von IAM-fähigen Services. Cloud Foundry-Services verfügen nicht über Verbindungen zu Ressourcengruppe und verwenden [Cloud Foundry-Rollen für das Zugriffsmanagement](/docs/iam?topic=iam-cfaccess#cfroles). Diese Services werden als Cloud Foundry-Services bezeichnet. Wenn für Services die Unterstützung für IAM und Ressourcengruppen aktiviert wird, werden Sie über die Möglichkeit benachrichtigt, [vorhandene Cloud Foundry-Instanzen in eine Ressourcengruppe zu migrieren](/docs/resources?topic=resources-migrate).


