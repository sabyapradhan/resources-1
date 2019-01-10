---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-15"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Foire aux questions
{: #resources-faq}

## Qu'est-ce qu'un groupe de ressources ?
{: #resource-group}
{: faq}

Un groupe de ressources permet d'organiser vos ressources de compte en regroupements personnalisables. Chaque ressource de compte gérée à l'aide du contrôle d'accès {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartient à un groupe de ressources au sein de votre compte. Lorsque vous créez des ressources à partir du catalogue, vous les affectez à un groupe de ressources. Vous pouvez alors consulter l'utilisation par groupe de ressources dans votre compte et affecter facilement l'accès utilisateur à toutes les ressources d'un groupe de ressources ou uniquement à une seule ressource d'un groupe.

Pour plus d'informations sur la création et l'utilisation des groupes de ressources, voir [Gestion des groupes de ressources](/docs/resources/resourcegroups.html#rgs).  

## Pourquoi dois-je migrer mes instances de service Cloud Foundry vers un groupe de ressources ?
{: #instance-migrated}
{: faq}

Le fait de migrer vos services Cloud Foundry vers un groupe de ressources fait que les services que vous utilisez sont désormais disponibles pour être utilisés avec les groupes de ressources et le contrôle d'accès IAM. Vous pouvez bénéficier du contrôle d'accès à granularité fine en utilisant des rôles IAM. Vous pouvez également consulter l'utilisation par groupe de ressources dans votre compte. 

Lorsque vous avez des services Cloud Foundry pouvant être migrés vers un groupe de ressources, vous recevez une notification dans votre liste de ressources. Pour plus d'informations sur le processus de migration, voir [Migration d'applications et d'instances de service dans un groupe de ressources](/docs/resources/instance_migration.html#migrate).

## Pourquoi ne puis-je pas créer de ressource et l'ajouter à un groupe de ressources ?
{: #create-add-resource}
{: faq}

Dans la plupart des cas, ce problème est lié à l'accès. Vous devez avoir au moins le rôle Afficheur pour le groupe de ressources et au moins le rôle Editeur pour le service du compte. Vous pouvez contacter l'administrateur du compte pour vérifier l'accès qui vous est affecté. 

## Qui peut créer des groupes de ressources ?
{: #create-resource}
{: faq}

Vous pouvez créer des groupes de ressources uniquement si vous disposez du rôle Administrateur pour tous les services activés par IAM {{site.data.keyword.Bluemix_notm}} dans le compte.

## Puis-je supprimer un groupe de ressources ?
{: #delete-resource-group}
{: faq}

Une fois un groupe de ressources créé, il n'est pas possible de le supprimer.

## Puis-je déplacer des instances de service entre différents groupes de ressources ?
{: #instances-between-rgs}
{: faq}

Vous ne pouvez pas déplacer des instances de service entre différents groupes de ressources. Si vous affectez une instance de service de manière incorrecte, vous devez supprimer et recréer l'instance afin de l'affecter au groupe de ressources correct.  

## Puis-je consulter l'utilisation par groupe de ressources ?
{: #view-usage}
{: faq}

Oui. Pour ouvrir la page Tableau de bord de l'utilisation, cliquez sur **Gérer** &gt; **Facturation et utilisation**. Sélectionnez **Utilisation** pour afficher un récapitulatif de l'utilisation par groupe de ressources pour le compte. 
