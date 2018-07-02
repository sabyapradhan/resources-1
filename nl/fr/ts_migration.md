---

copyright:

  years: 2018

lastupdated: "2018-06-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Traitement des incidents liés à la migration d'instances de service

Si vous rencontrez des problèmes lors de la migration d'une instance de service Cloud Foundry vers un groupe de ressources, passez en revue les problèmes courants présentés ci-après.

## Une instance de service a été migrée vers un groupe de ressources inapproprié

Vous ne pouvez pas déplacer des ressources entre des groupes de ressources une fois qu'elles sont affectées. Par conséquent, si vous avez affecté une instance à un groupe de ressources inapproprié, vous pouvez essayer de supprimer l'instance et d'en créer une nouvelle à partir du catalogue. Vous pouvez l'affecter au groupe de ressources approprié au moment où vous la créez.

## Un utilisateur du compte ne peut pas migrer d'instance éligible

Il se peut que vous ne disposiez pas des droits d'accès nécessaires pour faire migrer une instance de service. Pour plus d'informations, voir [Qui peut faire migrer des instances de service ?](/docs/resources/instance_migration.html#whocanmigrate).

## Tous les services ne sont pas éligibles à la migration

Les services ne peuvent pas tous être gérés et ajoutés à des groupes de ressources en utilisant Identity and Access Management. Vous recevez une notification lorsque les services sont éligibles, si vous disposez des droits d'accès nécessaires pour effectuer la migration.
