---

copyright:

  years: 2017, 2018

lastupdated: "2018-06-11"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migración de instancias de servicio de Cloud Foundry a un grupo de recursos
{: #migrate}

Para hacer su experiencia con el uso de {{site.data.keyword.Bluemix}} más simple y flexible, hemos introducido [grupos de recursos](/docs/resources/resourcegroups.html#rgs), que son conceptualmente similares a los espacios de Cloud Foundry. Sin embargo, los grupos de recursos incluyen varios beneficios adicionales, como el control de acceso más granular (mejor estructurado) utilizando IBM Cloud Identity and Access Management (IAM), la capacidad de conectar instancias de servicio a apps y servicios entre distintas regiones, y una forma sencilla de ver el uso por grupo.
{:shortdesc}

Estamos empezando a trasladar servicios desde Cloud Foundry para beneficiarse de los grupos de recursos, lo que significa que cuando seleccione el icono ![Migrar esta instancia de servicio a un grupo de recursos](images/migrate.svg "Migrar esta instancia de servicio a un grupo de recursos") junto a uno de los servicios del panel de control, debe iniciar un plan de migración para las instancias de servicio para trasladar desde la organización y el espacio actual de Cloud Foundry a un grupo de recursos. Hasta que un servicio de {{site.data.keyword.Bluemix_notm}} se traslade de utilizar organizaciones, espacios y roles de Cloud Foundry a utilizar IAM y grupos de recursos, no podrá migrar las instancias de servicios existentes de Cloud Foundry a un grupo de recursos.

Cuando migre instancias de servicio de Cloud Foundry a un grupo de recursos, no podrá cambiar el grupo que haya seleccionado una vez la migración se haya completado. Por lo tanto, es esencial que planifique cómo desea organizar los recursos en la cuenta antes de migrar. Esto puede requerir que cree uno o varios grupos de recursos, si dispone de una cuenta facturable, antes de realizar la migración. 

Puede intentar organizar sus recursos en grupos de recursos de la misma forma que se han organizado los recursos en los espacios de Cloud Foundry. Para obtener más información sobre cómo utilizar grupos de recursos, consulte [Mejores prácticas para la organización de recursos en grupos de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).
{: tip}


## ¿Por qué migrar instancias de servicio?

Los servicios que ofrecen soporte al control de acceso y organización de Cloud IAM en grupos de recursos disponen de varios beneficios:

* Al utilizar el control de acceso granular (estructurado), puede establecer el acceso a instancias de servicio individuales o un grupo de recursos organizado en un grupo de recursos. 
* Mediante los grupos de acceso y los grupos de recursos para organizar usuarios y recursos, establezca solo el número mínimo de políticas de acceso. Por ejemplo, si tiene un conjunto de desarrolladores a los que desea que tengan acceso a recursos para un entorno de desarrollo, puede organizar todos esos usuarios en un grupo de acceso de desarrolladores y, a continuación, añadir todos los recursos a los que necesitan acceder en un único grupo de recursos. A continuación, puede establecer una política única para el grupo de acceso para tener acceso a todos los recursos del grupo de recursos.
* Puede ver el uso por grupo de recursos de forma similar a la forma en la que puede ver el uso de las organizaciones de Cloud Foundry.
* Puede conectarse a apps y servicios en cualquier espacio de Cloud Foundry, lo que permite conexiones para apps y servicios de distintas regiones. Cuando realice la migración, la conexión se establecerá automáticamente convirtiendo su instancia de servicio de Cloud Foundry original en un alias y creando una instancia enlazada a un grupo de recursos de su elección. El gráfico siguiente describe cómo funciona la conexión utilizando un alias.

![Enlace de una instancia de servicio a un espacio de Cloud Foundry para crear un alias](images/alias.svg "Enlace de una instancia de servicio a un espacio de Cloud Foundry para crear un alias")

## ¿Quién puede migrar instancias de servicio?
{: #whocanmigrate}

Los usuarios deben tener acceso específico para migrar instancias de servicio de Cloud Foundry a un grupo de recursos:

* El usuario debe tener el rol de desarrollador en el espacio de Cloud Foundry o el rol de gestor de la organización de Cloud Foundry en la organización a la que pertenece la instancia.
* El usuario debe tener al menos el rol de IAM Visor para gestionar el grupo de recursos al que se va a migrar la instancia.
* El usuario debe tener al menos el rol de IAM Editor en el servicio.

Para obtener más información sobre la asignación del acceso correcto, consulte [Acceso de Cloud Foundry](/docs/iam/cfaccess.html#cfaccess) y [Acceso de IAM](/docs/iam/users_roles.html#platformrolestable).

Para comprobar qué acceso tiene, pulse **Gestionar** &gt; **Seguridad** &gt; **Identidad y acceso** en la barra de menús de la consola y pulse **Usuarios**. Pulse el nombre y revise las **Políticas de acceso** de los roles IAM asignados y el **Acceso de Cloud Foundry** para ver a qué organizaciones tiene acceso y los roles de Cloud Foundry que tiene asignados.
{: tip}


## ¿Cómo funciona la migración?

Cuando migra una instancia de servicio desde un espacio y organización de Cloud Foundry a un grupo de recursos, se crea en el grupo de recursos una nueva instancia de servicio enlazada. La instancia original de la organización y el espacio de Cloud Foundry pasa a ser un [alias](/docs/resources/connecting_apps.html#what_is_alias). El alias se tendrá en cuenta en relación con la cuota de su organización, pero se le facturará por el uso de la instancia de servicio en el grupo de recurso.

![Migración de una instancia de servicio de Cloud Foundry a un grupo de recursos](images/migration.gif){: gif}

Las instancias de servicio se migran de una en una cuando se lo notifique en el panel de control el icono ![Migrar esta instancia de servicios a un grupo de recursos](images/migrate.svg "Migrar esta instancia de servicio a un grupo de recursos") asociado a su instancia de servicio de Cloud Foundry.

Antes de iniciar el proceso de migración, revise la documentación del servicio para ver si hay alguna adicional, los cambios específicos del servicio que puede hacer cuando migra su instancia de servicio a un grupo de recursos. Por ejemplo, es posible que necesite migrar datos de instancias antiguas a nuevas instancias o actualizar las credenciales utilizadas para su app si suprime el alias de Cloud Foundry. Las aplicaciones que realicen una llamada directa a la API de un servicio que se ha migrado necesitan actualizar la llamada a la API para utilizar una clave de API IAM o una señal de acceso.
{: tip}

1. Abra el menú **Más acciones**.
2. Seleccione **Migrar a un grupo de recursos** para empezar.
3. Seleccione un grupo de recursos.
4. Pulse **Migrar** y la instancia se migrará.
5. Como solo puede migrar una instancia a la vez, puede continuar migrando instancias elegibles cuando haya realizado la migración de la primera.

Cuando haya migrado una instancia correctamente, la verá reflejada en la sección Servicio del panel de control. El alias permanecerá en la sección de Cloud Foundry del panel de control. Puede utilizar el ![Icono de enlace](images/link.svg "Icono de enlace que representa un alias") en la sección de Cloud Foundry del panel de control para identificar los alias.

## Pasos siguientes
{: #nextsteps}

Después de migrar sus instancias de servicio de Cloud Foundry a un grupo de recursos, debe asegurarse de que los usuarios de la cuenta tienen el nivel de acceso requerido a los recursos de los grupos de recursos de la cuenta. También es posible que desee proporcionar acceso para gestionar el grupo de recursos, de modo que los usuarios pueden crear nuevas instancias de servicio en los grupos de recursos de la cuenta.

Para obtener más información sobre la asignación de acceso a recursos de los grupos de recursos, consulte [Asignación de acceso a los grupos de recursos y a los recursos dentro de los mismos](/docs/resources/bestpractice_rgs.html#assigning-access-to-resource-groups-and-the-resources-within-them).

Además, asegúrese de revisar la documentación para el servicio para ver si se debe realizar alguna actualización para las apps existentes una vez que se complete la migración. 


## Resolución de problemas

Si se le presentan problemas al migrar instancias de servicio de Cloud Foundry, consulte [Resolución de problemas de migración de instancias de servicio](/docs/resources/ts_migration.html).
