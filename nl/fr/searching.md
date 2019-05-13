---

copyright:

  years: 2015, 2019
lastupdated: "2019-05-08"

keywords: search, find,

subcollection: resources, find resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# Recherche de ressources
{: #searching-for-resources}

Vous pouvez rechercher des ressources mises à disposition devant se trouver dans la liste des ressources et des offres dans le catalogue à partir de tout emplacement de la console {{site.data.keyword.cloud}}. Entrez la ressource ou l'étiquette dans la zone de recherche de la barre de menus de la console. Vous pouvez également utiliser l'interface de ligne de commande (CLI) {{site.data.keyword.Bluemix_notm}} pour effectuer une recherche dans vos ressources. L'interface CLI recherche des instances de service et des applications réparties dans différents emplacements et centres de données.
{:shortdesc}

## Affinage de vos résultats de recherche
{: #results}

<dl>
<dt>Afficher tous les résultats de ressource</dt>
<dd>Cette option permet d'afficher une liste de ressources filtrées qui charge automatiquement la zone de nom dans la liste de ressources. Vous disposez ainsi des résultats les plus pertinents. Le résultat de la recherche affiche les dix premiers résultats de ressource. Si vous savez que le nombre de résultats est plus important, vous pouvez accéder à la liste des ressources pour tous les consulter. Cette option s'affiche si elle correspond à un résultat de ressource ou à une recherche d'étiquette. Si elle ne correspond à aucune étiquette ou à aucun nom de résultat de ressource, elle ne s'affiche pas.</dd>
<dt>Afficher tous les résultats de catalogue</dt>
<dd>Cette option permet d'afficher une recherche de catalogue filtrée. Les cinq premiers résultats s'affichent par nom. Si vous souhaitez avoir un critère de recherche plus détaillé pour les entrées de catalogue, comme la recherche de la description, vous pouvez cliquer sur ce lien et obtenir une vue des résultats de catalogue filtrés. Cette option vous permet de trouver plus rapidement les offres que vous souhaitez créer. Elle s'affiche si elle correspond à un résultat de catalogue. Cette zone ne s'affiche pas si votre requête de recherche commence par `tag:`.</dd>
<dt>Rechercher dans les cas de support</dt>
<dd>Cette option permet de filtrer en fonction de vos cas de support ouverts au sein de la plateforme, notamment les ressources d'infrastructure. Elle s'affiche à la fin de la recherche, notamment si vous effectuez une recherche en utilisant `tag:`.</dd>
<dt>Rechercher dans la documentation IBM Cloud</dt>
<dd>Cette option permet d'obtenir une recherche filtrée de la documentation. Elle s'affiche à la fin de la recherche, notamment si vous effectuez une recherche en utilisant `tag:`.</dd>
</dl>

Appuyez sur la touche Barre oblique (/) pour positionner votre curseur dans la zone de recherche.
{: tip}


## Recherche avec l'interface de ligne de commande (CLI)
{: #searching-cl}

Vous pouvez également effectuer une recherche dans toutes vos ressources en utilisant la syntaxe de requête Lucene, avec une seule commande en utilisant l'interface CLI {{site.data.keyword.Bluemix_notm}} et ce à partir de la version 0.6.7.


Vous pouvez rechercher les attributs suivants :

<dl>
<dt>`name`</dt>
<dd> Nom défini par l'utilisateur de la ressource.</dd>
<dt>`region`</dt>
<dd>Emplacement géographique où la ressource est mise à disposition. Les valeurs autorisées sont les suivantes : `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` et `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>Nom du service, tel qu'il apparaît dans la colonne de nom de la sortie de l'élément 'ibmcloud catalog service-marketplace'.</dd>
<dt>`family`</dt>
<dd>Composant de cloud auquel votre ressource appartient. Les valeurs autorisées sont les suivantes : `cloud_foundry`, `containers`, `vmware`, `resource_controller` ou `ims`.</dd></dd>
<dt>`organization_id`</dt>
<dd>ID global unique de l'organisation Cloud Foundry.</dd>
<dt>`doc.space_id`</dt>
<dd>ID global unique de l'espace Cloud Foundry.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>ID du groupe de ressources.</dd>
<dt>`type                    `</dt>
<dd>Type de ressource. Les valeurs autorisées sont les suivantes : `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding`, `resource-group`, `vmware-solutions`, `cloud-object-storage-infrastructure`, `block-storage`, `file-storage` et `cloud-backup` .</dd>
<dt>`creation_date`</dt>
<dd>Date de création de la ressource.</dd>
<dt>`modification_date`</dt>
<dd> Date de dernière modification de la ressource.</dd>
<dt>`tags`</dt>
<dd>Etiquettes qui ont été associées à la ressource. </dd>
<dt>`tagReferences.tag.name`</dt>
<dd>Etiquettes qui ont été associées à la ressource d'infrastructure classique. Nécessite que vous indiquiez le paramètre `-p classic-infrastructure`. </dd>  
<dt>`_objectType:`</dt>
<dd>Type d'objet de la ressource d'infrastructure classique. Les valeurs autorisées sont les suivantes : `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall` et `SoftLayer_Virtual_Guest`. Nécessite que vous indiquiez le paramètre `-p classic-infrastructure`. </dd> 
</dl>

### Exemples de recherche
{: #resource-name}


Les exemples suivants peuvent vous aider lors de la recherche de ressources de compte.

* Pour rechercher toutes vos ressources nommées `ABC`, entrez la commande suivante :
    `ibmcloud resource search ‘name:ABC’`
  
* Pour rechercher toutes les applications Cloud Foundry nommées `MyResource`, entrez la commande suivante :

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* Pour rechercher toutes les instances de service du concentrateur de messages, entrez la commande suivante :

    `ibmcloud resource search 'service_name:messagehub'`

* Pour rechercher toutes les ressources dans l'organisation Cloud Foundry `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` ou le groupe de ressources `c900d9671b235c00461c5e311a8aeced` dans la région `us-south`, entrez la commande suivante :
    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`
    

* Pour rechercher des ressources qui ne font pas partie de l'infrastructure classique, qui ont été créées entre le 16 et le 20 mai 2018, entrez la commande suivante :
    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* Pour rechercher des ressources qui ne font pas partie de l'infrastructure classique dont le nom commence par "my", classées par type, entrez la commande suivante :

    `ibmcloud resource search 'name:my*' -s type`
    
* Pour rechercher des ressources qui ne font pas partie de l'infrastructure classique et qui ont été étiquetées avec `MyTag`, entrez la commande suivante :
    `ibmcloud resource search 'tags:MyTag'`
    
* Pour rechercher toutes les ressources de l'infrastructure classique qui ont été étiquetées avec `MyTag`, entrez la commande suivante :
    `ibmcloud resource search 'tagReferences.tag.name:MyTag' -p classic-infrastructure'`
    
* Pour rechercher toutes les ressources de l'infrastructure classique de type `Softlayer_Hardware`, entrez la commande suivante :
    `ibmcloud resource search '_objectType:SoftLayer_Hardware' -p classic-infrastructure'`
  

