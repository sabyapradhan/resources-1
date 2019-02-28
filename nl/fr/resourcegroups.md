---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# Gestion des groupes de ressources
{: #rgs}

Un groupe de ressources permet d'organiser vos ressources de compte en regroupements personnalisables de manière à pouvoir affecter rapidement des accès utilisateur à plusieurs ressources à la fois. Chaque ressource de compte gérée à l'aide du contrôle d'accès {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartient à un groupe de ressources au sein de votre compte. Les services Cloud Foundry sont affectés à des organisations et des espaces et ne peuvent pas être ajoutés à un groupe de ressources.

Pour commencer à gérer vos groupes de ressources, accédez à **Gérer** &gt; **Compte**. Développez **Ressources de compte** puis sélectionnez **Groupes de ressources**. Vous pouvez alors afficher vos groupes de ressources, ajouter des ressources, les renommer, gérer l'accès et créer de nouveaux groupes de ressources. Pour plus d'informations sur l'utilisation des groupes de ressources, voir [Meilleures pratiques pour l'organisation des ressources dans un groupe de ressources](/docs/resources?topic=resources-bp_resourcegroups).


## Création d'un groupe de ressources
{: #create_rgs}

Si vous disposez d'un compte Paiement à la carte ou Abonnement, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Vous pouvez également regrouper des ressources afin de faciliter l'affectation d'accès utilisateur à plusieurs instances à la fois. Il est important de noter que vous pouvez renommer un groupe de ressources, mais que vous ne pouvez pas le supprimer après sa création.

Si vous disposez d'un compte Lite ou d'un compte d'essai de 30 jours, vous ne pouvez pas créer de groupes de ressources supplémentaires, mais vous pouvez renommer votre groupe de ressources par défaut.

Les connexions entre un groupe de ressources et une organisation ou un espace Cloud Foundry sont restreintes par votre quota. Pour plus d'informations, voir [Qu'est-ce qu'un alias ?](/docs/resources?topic=resources-connect_app#what_is_alias).
{: note}

1. Accédez à **Gérer** &gt; **Compte**. Développez **Ressources de compte** puis sélectionnez **Groupes de ressources**. 
2. Cliquez sur **Créer un groupe de ressources**.
3. Entrez un nom pour le groupe de ressources.
4. Cliquez sur **Ajouter**.

## Ajout de ressources à un groupe de ressources
{: #add_to_rgs}

Les services gérés à l'aide d'IAM appartiennent à un groupe de ressources et non à une organisation ou un espace Cloud Foundry. Lorsque vous créez une instance de service pour l'un de ces services à partir du catalogue, vous êtes invité à affecter l'instance à un groupe de ressources. Votre sélection de groupe de ressource au moment de la création de l'instance est définitive et ne peut pas être modifiée.

Pour que les utilisateurs de votre compte puissent créer des ressources à partir du catalogue et les affecter à un groupe de ressources, deux règles d'accès doivent leur être affectées :

* Une règle avec rôle Afficheur ou supérieur appliquée au groupe de ressources lui-même
* Une règle avec rôle Editeur ou supérieur appliquée au service du compte

## Affichage des ressources des groupes de ressources
{: #view_rg_resources}

Pour afficher les ressources d'un groupe, effectuez un filtrage par groupe dans la liste de ressources.

## Modification du nom d'un groupe de ressources
{: #rename_rgs}

Votre premier groupe de ressources, automatiquement nommé `Default`, est créé. Vous pouvez modifier le nom de ce groupe ou de tout autre groupe que vous créez.

1. Accédez à **Gérer** &gt; **Compte**. Développez **Ressources de compte** puis sélectionnez **Groupes de ressources**. 
2. Sélectionnez **Renommer** dans le menu **Actions** ![Icône Liste des actions](../icons/action-menu-icon.svg).
3. Entrez un nom unique, puis cliquez sur **Sauvegarder**.

## Gestion des groupes de ressources et des ressources à l'aide de l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}
{: #rgs_cli}

L'interface de ligne de commande {{site.data.keyword.Bluemix_notm}} propose de nombreuses commandes de gestion des ressources. Pour plus d'informations, voir [Utilisation de ressources et de groupes de ressources](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource#ibmcloud_commands_resource).

## Gestion de l'accès à des groupes de ressources
{: #rgs_manage_access}

Cloud IAM vous offre la possibilité de fournir un accès utilisateur à granularité fine aux ressources de votre compte. Vous pouvez utiliser Cloud IAM pour affecter à des utilisateurs des règles qui donnent accès à toutes les ressources d'un groupe de ressources, à un seul type de service au sein d'un groupe de ressources ou à une instance de service individuelle du compte. Fournir un accès à des ressources au sein d'un groupe de ressources n'accorde pas aux utilisateurs concernés de droit de gestion du groupe de ressources lui-même. Vous pouvez définir séparément un accès permettant d'afficher, d'éditer et de gérer le groupe de ressources.

Pour plus d'informations, voir [Gestion de l'accès aux ressources](/docs/iam?topic=iam-iammanidaccser).
