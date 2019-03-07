---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: service instances, resource group, resource

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# リソースとは
{: #resource}

リソースとは、[リソース・グループ](/docs/resources?topic=resources-rgs)内に作成、管理、および含めることができるすべてのものです。 例としては、アプリ、サービス・インスタンス、コンテナー・クラスター、ストレージ・ボリューム、および仮想サーバーなどがあります。 カタログから作成される時にリソース・グループに追加できるすべてのサービス・インスタンスはリソースと呼ばれ、IAM アクセス制御を使用して管理されます。 リソース・グループ内の[アクセスのための IAM 役割](/docs/iam?topic=iam-userroles#iamusermanrol)と組織の使用をサポートするサービスは、IAM 対応サービスです。

現時点ですべてのサービスがリソース・グループおよび IAM の使用をサポートしているわけではありません。 カタログから作成された時に Cloud Foundry の組織およびスペースに追加されるすべてのサービス・インスタンスは、IAM 対応サービスとは明確に異なります。 Cloud Foundry サービスはリソース・グループとは関連がなく、[アクセス管理のために Cloud Foundry の役割](/docs/iam?topic=iam-cfaccess#cfroles)を使用します。 これらのサービスは、Cloud Foundry サービスと呼ばれます。 サービスで IAM およびリソース・グループのサポートが有効になると、[既存の Cloud Foundry インスタンスをリソース・グループにマイグレーション](/docs/resources?topic=resources-migrate)できることについて通知されます。
