---

copyright:

  years: 2018
lastupdated: "2018-06-19"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Qu'est-ce qu'une ressource ?
{: #resource}

Tout élément pouvant être créé, géré et inclus dans un [groupe de ressources](/docs/resources/resourcegroups.html#rgs) est appelé une ressource (application, instance de service, cluster de conteneurs et serveur virtuel, par exemple). Toutes les instances de service pouvant être ajoutées à un groupe de ressources lorsqu'elles sont créées à partir du catalogue sont appelées ressources et sont gérées via l'utilisation du contrôle d'accès IAM. Les services prenant en charge l'utilisation des [rôles IAM pour l'accès](/docs/iam/users_roles.html#iamusermanrol) et l'organisation dans un groupe de ressources sont des services activés par IAM.

Tous les services ne prennent pas actuellement en charge l'utilisation des groupes de ressources et d'IAM. Les instances de service ajoutées à des espaces et à des organisations Cloud Foundry lors de la création à partir du catalogue sont différentes des services activés par IAM. Les services Cloud Foundry ne sont pas liés aux groupes de ressources et ils utilisent les [rôles Cloud Foundry pour la gestion de l'accès](/docs/iam/cfaccess.html#cfaccess). Ces services sont appelés services Cloud Foundry. Comme les services activent le support d'IAM et des groupes de ressources, vous recevez des notifications sur la possibilité de [migrer des instances Cloud Foundry existantes vers un groupe de ressources](/docs/resources/instance_migration.html#migrate).

