---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: service instances, resource group, resource

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Qu'est-ce qu'une ressource ?
{: #resource}

Tout élément pouvant être créé, géré et inclus dans un [groupe de ressources](/docs/resources?topic=resources-rgs) est appelé une ressource (application, instance de service, cluster de conteneurs et serveur virtuel, par exemple). Toutes les instances de service pouvant être ajoutées à un groupe de ressources lorsqu'elles sont créées à partir du catalogue sont appelées ressources et sont gérées via l'utilisation du contrôle d'accès IAM. Les services prenant en charge l'utilisation des [rôles IAM pour l'accès](/docs/iam?topic=iam-userroles#iamusermanrol) et l'organisation dans un groupe de ressources sont des services activés par IAM.

Tous les services ne prennent pas actuellement en charge l'utilisation des groupes de ressources et d'IAM. Les instances de service ajoutées à des espaces et à des organisations Cloud Foundry lors de la création à partir du catalogue sont différentes des services activés par IAM. Les services Cloud Foundry ne sont pas liés aux groupes de ressources et ils utilisent les [rôles Cloud Foundry pour la gestion de l'accès](/docs/iam?topic=iam-cfaccess#cfroles). Ces services sont appelés services Cloud Foundry. Lorsque les services activent le support pour IAM et les groupes de ressources, vous recevez des notifications sur la possibilité de [migrer des instances Cloud Foundry existantes dans un groupe de ressources](/docs/resources?topic=resources-migrate).
