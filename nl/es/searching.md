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


# Búsqueda de recursos
{: #searching-for-resources}

Puede buscar recursos suministrados que espera encontrar en la lista de recursos y ofertas en el catálogo desde cualquier lugar de la consola de {{site.data.keyword.cloud}}. Escriba el recurso o la etiqueta en el campo de búsqueda de la barra de menús de la consola. También puede utilizar la interfaz de línea de mandatos (CLI) de {{site.data.keyword.Bluemix_notm}} para buscar entre sus recursos. La CLI busca aplicaciones distribuidas e instancias de servicio en ubicaciones y centros de datos.
{:shortdesc}

## Limitación de los resultados de la búsqueda
{: #results}

<dl>
<dt>Ver todos los resultados de recursos</dt>
<dd>Utilice esta opción para ver una lista de recursos filtrados que especifica automáticamente el campo de nombre en la lista de recursos, ofreciéndole así los resultados más relevantes. La búsqueda devuelta muestra los 10 primeros resultados de recursos. Si sabe que hay más resultados, puede verlos todos en la lista de recursos. Esta opción aparece si coincide con la búsqueda de un resultado de recursos o de una etiqueta. Si no coincide con un nombre de resultado de recurso o con una etiqueta, no aparece.</dd>
<dt>Ver todos los resultados del catálogo</dt>
<dd>Utilice esta opción para ver una búsqueda de catálogo filtrada. Los primeros cinco resultados se muestran por su nombre. Si desea un criterio de búsqueda más detallado para las entradas de catálogo, como por ejemplo buscar la descripción, puede pulsar este enlace y obtener una vista de resultados de catálogo filtrada. Esta opción le ayuda a encontrar con mayor rapidez las ofertas que desea crear. Esta opción aparece si coincide con un resultado de catálogo. Este campo no aparece si la consulta de búsqueda empieza por `tag:`.</dd>
<dt>Casos de soporte de búsqueda</dt>
<dd>Utilice esta opción para filtrar por los casos de soporte abierto en toda la plataforma, incluidos los recursos de la infraestructura. Esto aparece al final de la búsqueda si busca algo, incluso si busca por `tag:`.</dd>
<dt>Buscar en la documentación de IBM Cloud</dt>
<dd>Utilice esta opción para realizar una búsqueda filtrada de la documentación. Esto aparece al final de la búsqueda si busca algo, incluso si busca por `tag:`.</dd>
</dl>

Pulse la tecla de barra inclinada (/) para mover el cursor al campo de búsqueda.
{: tip}


## Búsqueda con la CLI
{: #searching-cl}

También puede buscar entre todos los recursos utilizando la sintaxis de consulta de Lucene, con un solo mandato mediante la CLI de {{site.data.keyword.Bluemix_notm}}, a partir de la versión 0.6.7.


Puede buscar los siguientes atributos:

<dl>
<dt>`nombre`</dt>
<dd> El nombre del recurso definido por el usuario.</dd>
<dt>`región`</dt>
<dd>La ubicación geográfica en la que se suministra el recurso. Los valores permitidos son `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` y `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>El nombre del servicio, tal como aparece en la columna Nombre de la salida de 'ibmcloud catalog service-marketplace'.</dd>
<dt>`family`</dt>
<dd>El componente de nube al que pertenece el recurso. Los valores permitidos son `cloud_foundry`, `containers`, `vmware`, `resource_controller` o `ims`.</dd></dd>
<dt>`organization_id`</dt>
<dd>La GUID de la organización de Cloud Foundry.</dd>
<dt>`doc.space_id`</dt>
<dd>El GUID del espacio de Cloud Foundry.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>El ID del grupo de recursos.</dd>
<dt>`type`</dt>
<dd>El tipo de recurso. Los valores permitidos son `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding`, `resource-group`, `vmware-solutions`, `cloud-object-storage-infrastructure`, `block-storage`, `file-storage`, `cloud-backup`.</dd>
<dt>`creation_date`</dt>
<dd>La fecha en que se ha creado el recurso.</dd>
<dt>`modification_date`</dt>
<dd> La fecha de la última modificación del recurso.</dd>
<dt>`tags`</dt>
<dd>Las etiquetas que se han adjuntado al recurso </dd>
<dt>`tagReferences.tag.name`</dt>
<dd>Las etiquetas que se han adjuntado a un recurso de la infraestructura clásica. Debe especificar el parámetro `-p classic-infrastructure`. </dd>  
<dt>`_objectType:`</dt>
<dd>El tipo de objeto del recurso de la infraestructura clásica. Los valores permitidos son: `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest`. Debe especificar el parámetro `-p classic-infrastructure`. </dd> 
</dl>

### Ejemplos de búsquedas
{: #resource-name}


Los ejemplos siguientes pueden ayudarle a buscar recursos de la cuenta.

* Para buscar todos los recursos llamados `ABC`, especifique el mandato siguiente: `ibmcloud resource search ‘name:ABC’`
  
* Para buscar todas las aplicaciones de Cloud Foundry llamadas `MyResource`, especifique el mandato siguiente:

    `ibmcloud resource search 'name:my* AND type:cf-application'`

* Para buscar todas las instancias de servicio de Message Hub, especifique el mandato siguiente:

    `ibmcloud resource search 'service_name:messagehub'`

* Para buscar todos los recursos de la organización de Cloud Foundry `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` o del grupo de recursos `c900d9671b235c00461c5e311a8aeced` en la región `us-south`, especifique el siguiente mandato: `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`
    

* Para buscar recursos que no sean la infraestructura clásica que se han creado entre el 16 de mayo de 2018 y el 20 de mayo de 2018, especifique el mandato siguiente: `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* Para buscar recursos que no sean una infraestructura clásica cuyo nombre empiece por "my", ordenados por tipo, especifique el mandato siguiente:

    `ibmcloud resource search 'name:my*' -s type`
    
* Para buscar recursos que no sean de la infraestructura clásica que se hayan etiquetado con `MyTag`, especifique el siguiente mandato: `ibmcloud resource search 'tags:MyTag'`
    
* Para buscar todos los recursos de la infraestructura clásica que se hayan etiquetado con `MyTag`, especifique el siguiente mandato: `ibmcloud resource search 'tagReferences.tag.name:MyTag' -p classic-infrastructure'`
    
* Para buscar todos los recursos de la infraestructura clásica de tipo `Softlayer_Hardware`, escriba:
    `ibmcloud resource search '_objectType:SoftLayer_Hardware' -p classic-infrastructure'`
  

