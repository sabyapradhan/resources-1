---

copyright:

  years: 2015, 2019

lastupdated: "2019-05-21"

keywords: resource FAQs, resource frequently asked questions

subcollection: resources

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

Pour plus d'informations sur la création et l'utilisation des groupes de ressources, voir [Gestion des groupes de ressources](/docs/resources?topic=resources-rgs).  

## Pourquoi dois-je migrer mes instances de service Cloud Foundry vers un groupe de ressources ?
{: #instance-migrated}
{: faq}

Le fait de migrer vos services Cloud Foundry vers un groupe de ressources fait que les services que vous utilisez sont désormais disponibles pour être utilisés avec les groupes de ressources et le contrôle d'accès IAM. Vous pouvez bénéficier du contrôle d'accès à granularité fine en utilisant des rôles IAM. Vous pouvez également consulter l'utilisation par groupe de ressources dans votre compte. 

Lorsque vous avez des services Cloud Foundry pouvant être migrés vers un groupe de ressources, vous recevez une notification dans votre liste de ressources. Pour plus d'informations sur le processus de migration, voir [Migration d'applications et d'instances de service dans un groupe de ressources](/docs/resources?topic=resources-migrate).

## Pourquoi ne puis-je pas ajouter de ressource à un groupe de ressources ?
{: #create-add-resource}
{: faq}

Dans la plupart des cas, ce problème est lié à l'accès. Vous devez avoir au moins le rôle Afficheur pour le groupe de ressources et au moins le rôle Editeur pour le service du compte. Pour en savoir plus, consultez la rubrique [Ajout de ressources à un groupe de ressources](/docs/resources?topic=resources-rgs#add_to_rgs).

Pour plus d'informations sur la vérification de votre accès affecté, voir [Révision des accès affectés](/docs/iam?topic=iam-iammanidaccser#review_your_access).

Si vous avez besoin d'un accès supplémentaire au compte, contactez le propriétaire du compte indiqué sur la page des [utilisateurs](https://{DomainName}/iam#/users). 

## Qui peut créer des groupes de ressources ?
{: #create-resource}
{: faq}

Vous pouvez créer des groupes de ressources uniquement si vous disposez du rôle Administrateur pour tous les services de gestion des comptes dans le compte.

Les comptes Lite ne peuvent inclure que le groupe de ressources par défaut. Vous ne pouvez donc pas créer de groupe de ressources supplémentaire même si vous disposez de l'accès requis.

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

## Qui peut ajouter des étiquettes à une ressource ?
{: #tag-fag}
{: faq}

Tout utilisateur disposant de l'accès correct pour le type spécifique de ressource peut ajouter des étiquettes. Lorsqu'une ressource est étiquetée, elle est visible par tous les utilisateurs ayant un accès en lecture à la ressource. Cependant, pour ajouter ou retirer une étiquette à une ressource, certains droits ou rôles d'accès sont requis en fonction du type de ressource. Par exemple, pour les ressources gérées via IAM, le rôle Editeur ou Administrateur doit vous être affecté pour la ressource. Pour plus d'informations sur l'accès requis pour les autres types de ressource, voir [Droits d'étiquetage](/docs/resources?topic=resources-access#tagging-permissions).
