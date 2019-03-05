---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-07"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Preguntas más frecuentes
{: #resources-faq}

## ¿Qué es un grupo de recursos?
{: #resource-group}
{: faq}

Un grupo de recursos es una manera de organizar sus recursos de cuenta en agrupaciones personalizables. Cualquier recurso de cuenta gestionado utilizando el control de acceso de la Gestión de identidad y acceso de {{site.data.keyword.Bluemix}} pertenece a un grupo de recursos dentro de su cuenta. Asigna recursos a un grupo de recursos cuando los crea desde el catálogo. A continuación, puede ver el uso por grupo de recursos en la cuenta y asignar fácilmente acceso de usuario a todos los recursos de un grupo de recursos, o solo a un único recurso de un grupo de recursos.

Para obtener más información sobre cómo crear y trabajar con grupos de recursos, consulte [Gestionar grupos de recursos](/docs/resources/resourcegroups.html#rgs).  

## ¿Por qué debería migrar mis instancias de servicio de Cloud Foundry a un grupo de recursos?
{: #instance-migrated}
{: faq}

La migración de los servicios de Cloud Foundry a un grupo de recursos significa que los servicios que está utilizando están ahora disponibles para su uso con grupos de recursos y control de acceso de IAM. Puede aprovechar el control de acceso granular mediante roles de IAM. También puede ver el uso por grupo de recursos en su cuenta. 

Cuando tenga servicios de Cloud Foundry que se puedan migrar a un grupo de recursos, recibirá una notificación en la lista de recursos. Para obtener más información sobre el proceso de migración, consulte [Migración de instancias de servicio y apps de Cloud Foundry a un grupo de recursos](/docs/resources/instance_migration.html#migrate).

## ¿Por qué no puedo crear un recurso y añadirlo a un grupo de recursos?
{: #create-add-resource}
{: faq}

Lo más probable es que tenga un problema de acceso. Debe tener, como mínimo, el rol Visor en el propio grupo de recursos y, como mínimo, el rol Editor en el servicio de la cuenta. Encontrará más información en [Adición de recursos a un grupo de recursos](/docs/resources/resourcegroups.html#adding-resources-to-a-resource-group).

Para obtener más información sobre cómo comprobar el acceso asignado, consulte [Revisión del acceso asignado](/docs/iam/mngiam.html#reviewing-your-assigned-access).

Si necesita acceso adicional en la cuenta, póngase en contacto con el propietario de la cuenta que se muestra en la página [Usuarios](https://{DomainName}/iam#/users). 

## ¿Quién puede crear grupos de recursos?
{: #create-resource}
{: faq}

Solo puede crear grupos de recursos si se le asigna el rol Administrador en todos los servicios habilitados para {{site.data.keyword.Bluemix_notm}} Identity and Access en la cuenta.

## ¿Puedo suprimir un grupo de recursos?
{: #delete-resource-group}
{: faq}

No se puede suprimir un grupo de recursos después de haberlo creado.

## ¿Puedo mover instancias de servicio entre grupos de recursos?
{: #instances-between-rgs}
{: faq}

No puede mover instancias de servicio entre grupos de recursos. Si asigna una instancia de servicio de forma incorrecta, tiene que suprimir y volver a crear la instancia para asignarla al grupo de recursos correcto.  

## ¿Puedo ver el uso por grupo de recursos?
{: #view-usage}
{: faq}

Sí, puede. Para abrir la página Panel de control de uso, pulse **Gestionar** &gt; **Facturación y uso**. Seleccione **Uso** para ver un resumen del uso por grupo de recursos para la cuenta. 
