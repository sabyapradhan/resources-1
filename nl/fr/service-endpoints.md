---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-28"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Noeuds finaux de service pour connexions de réseau privé
{: #service-endpoints}

Une attention accrue en matière de sécurité est requise de la part des clients utilisant des services cloud pour les charges de travail de production. Pour de nombreux clients, l'accès aux services de manière sécurisée n'est pas seulement une politique d'entreprise judicieuse mais il s'agit aussi, dans certains cas, d'une obligation de conformité à des réglementations en vigueur. {{site.data.keyword.IBM_notm}} a amélioré les options de connectivité pour les clients qui nécessitent des options de connectivité isolées pour leurs charges de travail. 

Avec les noeuds finaux de service {{site.data.keyword.cloud}}, vous pouvez vous connecter aux services {{site.data.keyword.cloud_notm}} via le réseau privé d'{{site.data.keyword.cloud_notm}}. Déplacez ces charges de travail depuis le réseau public offre deux avantages :

* Les services ne sont plus utilisés sur une adresse IP routable sur Internet. De plus en plus, les clients du cloud ne veulent aucun accès ou un accès limité à l'Internet public à partir d'un de leurs services. Désormais, avec la fonction de noeud final de service, les équipes chargées des services peuvent créer une interface via le réseau privé pour leurs services que les clients peuvent utiliser pour se connecter. L'accès Internet n'est plus une condition requise pour se connecter aux services {{site.data.keyword.cloud_notm}}.
* Il n'y a pas de frais liés à la bande passante utilisée facturables sur le réseau privé. Auparavant, vous étiez facturé pour la bande passante sortante lorsque vous communiquiez avec un service {{site.data.keyword.cloud_notm}}. 

La figure suivante montre comment le trafic est acheminé via le réseau privé d'{{site.data.keyword.cloud_notm}} lors de l'accès aux services cloud via les noeuds finaux de service :

![Noeud final de service IBM Cloud](images/CSE.png "Trafic acheminé via un noeud final de service")

Pour utiliser des noeuds finaux de service {{site.data.keyword.cloud_notm}}, vous devez activer la fonction de routage et transfert virtuel (VRF) dans votre compte. Vous pouvez ensuite activer l'utilisation des noeuds finaux de service. Une fois que les deux options sont activées, vous pouvez commencer à créer des services qui prennent en charge l'utilisation de la fonction VRF et des noeuds finaux de service du catalogue. Pour plus d'informations, voir [Activation de VRF et des noeuds finaux de service](/docs/account?topic=account-vrf-service-endpoint).
