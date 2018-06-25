---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Traitement des incidents liés à la migration d'instances de service

Si vous rencontrez des problèmes lors de la migration d'une instance de service Cloud Foundry vers un groupe de ressources, passez en revue les problèmes courants présentés ci-après pour pouvoir continuer votre processus de migration.

## Que se passe-t-il si j'ai fait migrer mon instance de service vers un groupe de ressources inapproprié ?

A l'heure actuelle, vous ne pouvez pas déplacer des ressources entre des groupes de ressources une fois qu'elles sont affectées. Par conséquent, si vous avez fait migrer une instance vers un groupe de ressources inapproprié, vous pouvez essayer de supprimer l'instance et d'en créer une nouvelle à partir du catalogue. Vous pouvez l'affecter au groupe de ressources approprié au moment où vous la créez.

## Pour quelle raison la procédure de migration échoue-t-elle ?

Il se peut que vous ne disposez des droits d'accès nécessaires pour faire migrer une instance de service. Pour plus d'informations, voir [Qui peut faire migrer des instances de service](/docs/account/instance_migration.html#whocanmigrate).

## Pour quelle raison mes services ne sont-ils pas tous éligibles pour migration ?

A l'heure actuelle, les services ne sont pas tous disponibles pour être gérés via le contrôle d'accès IAM et les groupes de ressources. Vous êtes avisé quand des services permettent l'utilisation d'IAM, si vous disposez des droits d'accès nécessaires pour effectuer la migration.
