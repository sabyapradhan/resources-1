---

copyright:

  years: 2018
lastupdated: "2018-07-17"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# リソースとは
{: #resource}

リソースとは、[リソース・グループ](/docs/resources/resourcegroups.html#rgs)内に作成、管理、および含めることができるすべてのものです。 例としては、アプリ、サービス・インスタンス、コンテナー・クラスター、ストレージ・ボリューム、および仮想サーバーなどがあります。 カタログから作成される時にリソース・グループに追加できるすべてのサービス・インスタンスはリソースと呼ばれ、IAM アクセス制御を使用して管理されます。 リソース・グループ内の[アクセスのための IAM 役割](/docs/iam/users_roles.html#iamusermanrol)と組織の使用をサポートするサービスは、IAM 対応サービスです。

現時点ですべてのサービスがリソース・グループおよび IAM の使用をサポートしているわけではありません。 カタログから作成された時に Cloud Foundry の組織およびスペースに追加されるすべてのサービス・インスタンスは、IAM 対応サービスとは明確に異なります。 Cloud Foundry サービスはリソース・グループとは関連がなく、[アクセス管理のために Cloud Foundry の役割](/docs/iam/cfaccess.html#cfaccess)を使用します。 これらのサービスは、Cloud Foundry サービスと呼ばれます。 サービスで IAM およびリソース・グループのサポートが有効になると、[既存の Cloud Foundry インスタンスをリソース・グループにマイグレーション](/docs/resources/instance_migration.html#migrate)できることが通知されます。

