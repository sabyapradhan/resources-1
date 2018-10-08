---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Traitement des incidents liés aux services et aux ressources
{: #services}

Les problèmes liés aux services {{site.data.keyword.Bluemix}} peuvent inclure des incidents lors de la suppression d'instances de service. Ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}

## Pour quelle raison la suppression d'instance de service échoue-t-elle ?
{: #ts_service_broker}

Il se peut que vous receviez un message d'erreur si vous tentez de supprimer une instance de service qui a déjà été supprimée du contrôleur de cloud.
{:shortdesc}

Lorsque vous tentez de supprimer une instance de service, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`Gateway timeout`

Ce problème se produit lorsque l'instance de service a déjà été supprimée du contrôleur de cloud.
{: tsCauses}

Créez une instance de service portant le même nom de service puis liez-la à vos applications. Vous pouvez ensuite supprimer l'instance de service et les applications qui utilisent ce service.   
{: tsResolve}
