---

copyright:

  years: 2018

lastupdated: "2018-05-09"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# 移轉服務實例的疑難排解

如果您在將 Cloud Foundry 服務實例移轉至資源群組時遇到任何問題，請檢閱下列一般問題，以協助您繼續移轉。

## 我將服務實例移轉至錯誤的資源群組怎麼辦？

目前，您在指派資源之後，就無法在資源群組之間移動資源。因此，如果您將實例移轉至錯誤的資源群組，您可以嘗試刪除該實例，並從型錄中建立新的實例。您可以在建立實例時，將它指派給正確的資源群組。

## 為何無法移轉？

您可能未被指派正確的存取權，以便移轉服務實例。如需相關資訊，請參閱[誰可以移轉服務實例](/docs/account/instance_migration.html#whocanmigrate)。

## 為什麼不是所有服務都適用於移轉？

目前並非所有服務都可以透過使用 IAM 存取控制及資源群組進行管理。如果您具有完成移轉作業的存取權，則會在服務啟用 IAM 時通知您。
