---

copyright:

  years: 2015, 2019

lastupdated: "2019-04-11"

keywords: resource FAQs, resource frequently asked questions

subcollection: resources

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

Un grupo de recursos es una manera de organizar sus recursos de cuenta en agrupaciones personalizables. Cualquier recurso de cuenta gestionado utilizando el control de acceso de {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) pertenece a un grupo de recursos dentro de su cuenta. Asigna recursos a un grupo de recursos cuando los crea desde el catálogo. A continuación, puede ver el uso por grupo de recursos en la cuenta y asignar fácilmente acceso de usuario a todos los recursos de un grupo de recursos, o solo a un único recurso de un grupo de recursos.

Para obtener más información sobre cómo crear y trabajar con grupos de recursos, consulte [Gestionar grupos de recursos](/docs/resources?topic=resources-rgs).  

## ¿Por qué debería migrar mis instancias de servicio de Cloud Foundry a un grupo de recursos?
{: #instance-migrated}
{: faq}

La migración de los servicios de Cloud Foundry a un grupo de recursos significa que los servicios que está utilizando están ahora disponibles para su uso con grupos de recursos y control de acceso de IAM. Puede aprovechar el control de acceso granular mediante roles de IAM. También puede ver el uso por grupo de recursos en su cuenta. 

Cuando tenga servicios de Cloud Foundry que se puedan migrar a un grupo de recursos, recibirá una notificación en la lista de recursos. Para obtener más información sobre el proceso de migración, consulte [Migración de instancias de servicio y apps de Cloud Foundry a un grupo de recursos](/docs/resources?topic=resources-migrate).

## ¿Por qué no puedo añadir un recurso a un grupo de recursos?
{: #create-add-resource}
{: faq}

Lo más probable es que tenga un problema de acceso. Debe tener, como mínimo, el rol Visor en el propio grupo de recursos y, como mínimo, el rol Editor en el servicio de la cuenta. Encontrará más información en [Adición de recursos a un grupo de recursos](/docs/resources?topic=resources-rgs#add_to_rgs).

Para obtener más información sobre cómo comprobar el acceso asignado, consulte [Revisión del acceso asignado](/docs/iam?topic=iam-iammanidaccser#review_your_access).

Si necesita acceso adicional en la cuenta, póngase en contacto con el propietario de la cuenta que se muestra en la página [Usuarios](https://{DomainName}/iam#/users). 

## ¿Quién puede crear grupos de recursos?
{: #create-resource}
{: faq}

Solo puede crear grupos de recursos si se le asigna el rol Administrador en todos los servicios habilitados para {{site.data.keyword.Bluemix_notm}} Identity and Access en la cuenta.

Las cuentas Lite solo pueden tener el grupo de recursos predeterminado, por lo que no puede crear grupos de recursos adicionales aunque tenga el acceso necesario.

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

## ¿Quién puede añadir etiquetas a un recurso?
{: #tag-fag}
{: faq}

Cualquier usuario que tenga asignado los permisos correctos de acceso al tipo de recurso específico puede añadir etiquetas. Cuando se etiqueta un recurso, es visible para todos los usuarios que tienen acceso de lectura al recurso. Sin embargo, para añadir o eliminar una etiqueta de un recurso, se necesitan ciertos roles o permisos que dependen del tipo de recurso. Por ejemplo, para los recursos que están gestionados mediante IAM, debe tener asignado el rol de Editor o Administrador en el recurso. Para obtener más información sobre el acceso necesario a otros tipos de recurso, consulte [Permisos de etiquetado](/docs/resources?topic=resources-access#tagging-permissions).
