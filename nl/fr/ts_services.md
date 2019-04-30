---

copyright:

  years: 2015, 2019

lastupdated: "2019-03-11"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, error message

subcollection: resources

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Traitement des incidents liés aux services et aux ressources
{: #services}

Les problèmes d'ordre général liés aux services et aux ressources peuvent inclure des problèmes survenant lors de la suppression des instances de service ou de la migration des services. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}

## Pour quelle raison la suppression d'instance de service échoue-t-elle ?
{: #ts_service_broker}
{: troubleshoot}

Il se peut que vous receviez un message d'erreur si vous tentez de supprimer une instance de service qui a déjà été supprimée du contrôleur de cloud.
{:shortdesc}

Lorsque vous tentez de supprimer une instance de service, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`Gateway timeout`

Ce problème se produit lorsque l'instance de service a déjà été supprimée du contrôleur de cloud.
{: tsCauses}

Créez une instance de service portant le même nom de service puis liez-la à vos applications. Vous pouvez ensuite supprimer l'instance de service et les applications qui utilisent ce service.   
{: tsResolve}

## Pourquoi une instance de service a-t-elle été migrée vers un groupe de ressources incorrect ? 
{: #ts_service_instance}
{: troubleshoot}

Vous pouvez remarquer qu'une instance de service a été migrée vers un groupe de ressources incorrect et ne peut pas être réaffectée. 
{:shortdesc}

Vous ne pouvez pas déplacer des ressources entre des groupes de ressources une fois qu'elles sont affectées.
{: tsSymptoms}

Vous avez affecté l'instance à un groupe de ressources incorrect.  
{: tsCauses}

Pour corriger ce problème, vous pouvez tenter de supprimer l'instance et d'en créer une nouvelle à partir du catalogue. Lors de la création de la nouvelle instance, vous pouvez l'affecter au groupe de ressources correct.
{: tsResolve}

## Pourquoi ne puis-je pas migrer une instance de service Cloud Foundry éligible vers un groupe de ressources ?
{: #ts_migrate_instance}
{: troubleshoot}

En tant qu'utilisateur du compte, vous rencontrez des problèmes lors de la migration d'une instance éligible. 
{:shortdesc}

Vous ne pouvez pas migrer une instance éligible. 
{: tsSymptoms}

Si vous ne pouvez pas migrer une instance éligible, il est possible que vous ne disposiez pas de l'accès correct. 
{: tsCauses}

Les utilisateurs doivent avoir un accès spécifique pour migrer une instance. Pour vérifier l'accès dont vous disposez, cliquez sur **Gérer** &gt; **Accès (IAM)** dans la barre de menus de la console puis cliquez sur **Utilisateurs**. Cliquez sur votre nom et passez en revue vos règles d'accès pour les rôles IAM affectés et les droits d'accès Cloud Foundry afin de voir les organisations auxquelles vous avez accès, ainsi que les rôles Cloud Foundry qui vous sont affectés. 
{: tsResolve}

## Pourquoi ne puis-je pas migrer tous mes services ?
{: #ts_service_migration}
{: troubleshoot}

Tous les services ne sont pas éligibles pour la migration. 
{:shortdesc}

Vous ne pouvez pas migrer certains services. 
{: tsSymptoms}

Vous tentez de migrer des services qui ne sont pas disponibles pour être ajoutés aux groupes de ressources et qui ne sont pas gérés via l'utilisation d'IAM (Identity and Access Management). Si aucun service n'est éligible, la migration n'est pas possible. 
{: tsCauses}

Vérifiez les services pour confirmer qu'ils sont éligibles pour la migration. Vous recevez une notification et une icône ![Migration de cette instance de service vers un groupe de ressources](images/migrate.svg "Migration de cette instance de service vers un groupe de ressources") signale si un service est éligible pour la migration.
{: tsResolve}
