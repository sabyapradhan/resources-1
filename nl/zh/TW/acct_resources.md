---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# 何謂資源？
{: #resource}

資源是可以在[資源群組](/docs/resources?topic=resources-rgs)中建立、管理及包含在其中的任何項目。部分範例包括應用程式、服務實例、容器叢集、儲存空間磁區和虛擬伺服器。在從型錄建立時可以新增至資源群組的所有服務實例，皆稱為資源，並且使用 IAM 存取控制來加以管理。支援使用 [IAM 角色進行存取](/docs/iam?topic=iam-userroles#iamusermanrol)並組織在資源群組內的服務，即為已啟用 IAM 的服務。

目前並非所有服務都支援使用資源群組和 IAM。在從型錄建立時新增至 Cloud Foundry 組織和空間的所有服務實例，與已啟用 IAM 的服務截然不同。Cloud Foundry 服務與資源群組沒有關聯，並且是使用 [Cloud Foundry 角色來進行存取管理](/docs/iam?topic=iam-cfaccess#cfroles)。這些服務稱為 Cloud Foundry 服務。當服務啟用對 IAM 和資源群組的支援時，系統會通知您可以[將現有的 Cloud Foundry 實例移轉至資源群組](/docs/resources?topic=resources-migrate)。


