---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-15"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# Gestionar grupos de recursos
{: #rgs}

Un grupo de recursos es una manera de organizar sus recursos de cuenta en agrupaciones personalizables para que pueda asignar accesos de usuario rápidamente a más de un recurso a la vez. Cualquier recurso de cuenta gestionado utilizando el control de acceso de la Gestión de identidad y acceso de {{site.data.keyword.Bluemix}} pertenece a un grupo de recursos dentro de su cuenta. Los servicios de Cloud Foundry se asignan a organizaciones o espacios y no se pueden añadir a un grupo de recursos.

Para empezar a gestionar sus grupos de recursos, vaya a **Gestionar** &gt; **Cuenta**. Amplíe los **Recursos de cuenta** y luego seleccione **Grupos de recursos**. Desde ahí puede ver sus grupos de recursos, añadir recursos, cambiarles el nombre, gestionar accesos y crear nuevos grupos de recursos. Para obtener más información sobre cómo trabajar con grupos de recursos, consulte [Mejores prácticas para organizar los recursos en grupos de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).


## Creación de un grupo de recursos

Si tiene una cuenta de Pago según uso o de Suscripción, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. También puede agrupar recursos para facilitarles la asignación de acceso a los usuarios a más de una instancia a la vez. Es importante tener en cuenta que puede cambiar el nombre de un grupo de recursos, pero no puede suprimir un grupo de recursos una vez creado.

Si tiene una cuenta Lite o una prueba de 30 días, no puede crear grupos de recursos adicionales pero puede renombrar su grupo de recursos predeterminado.

Las conexiones entre un grupo de recursos y una organización de Cloud Foundry o espacio están restringidas por su cuota. Para obtener más información, consulte [¿Qué es un alias?](/docs/resources/connecting_apps.html#what_is_alias)
{: note}

1. Vaya a **Gestionar** &gt; **Cuenta**. Amplíe los **Recursos de cuenta** y luego seleccione **Grupos de recursos**. 
2. Pulse **Crear un grupo de recursos**.
3. Especifique un nombre para su grupo de recursos.
4. Pulse **Añadir**.

## Adición de recursos a un grupo de recursos

Los servicios gestionados con IAM pertenecen a un grupo de recursos en lugar de a una organización o espacio de Cloud Foundry. Cuando cree una instancia de servicio para uno de los servicios del catálogo, se le solicitará que asigne la instancia a un grupo de recursos. La selección del grupo de recursos en el momento de crear la instancia es definitiva y no se puede cambiar.

## Visualización de recursos dentro de grupos de recursos

Para ver fácilmente los recursos contenidos en un grupo de recursos, filtre por grupo de recursos desde su lista de recursos.

## Cómo renombrar un grupo de recursos

Su primer grupo de recursos se crea y se llama `Default`. Puede actualizar el nombre de este grupo o cualquier otro grupo que cree.

1. Vaya a **Gestionar** &gt; **Cuenta**. Amplíe los **Recursos de cuenta** y luego seleccione **Grupos de recursos**. 
2. Seleccione **Renombrar** en el menú **Acciones** ![Icono de lista de acciones](../icons/action-menu-icon.svg).
3. Especifique un nombre exclusivo y pulse **Guardar**.

## Gestión de grupos de recursos utilizando la CLI de {{site.data.keyword.Bluemix_notm}}

La CLI de {{site.data.keyword.Bluemix_notm}} tiene varios mandatos que soportan la gestión de recursos. Para obtener más información, consulte [Cómo trabajar con recursos y grupos de recursos](/docs/cli/reference/ibmcloud/cli_resource_group.html#ibmcloud_commands_resource).

## Gestión del acceso a sus grupos de recursos

Cloud IAM le ofrece la flexibilidad de proporcionar acceso de usuario preciso a recursos en su cuenta. Puede utilizar Cloud IAM para asignar políticas a usuarios, que proporcionan acceso de usuario a todos los recursos de un grupo de recursos, a un único tipo de servicio dentro de un grupo de recursos o a una instancia de servicio individual en su cuenta. Proporcionar acceso a los usuarios a los recursos en un grupo de recursos no les da acceso para gestionar el grupo de recursos en sí mismo. Puede establecer accesos para las capacidades de ver, editar y gestionar el grupo de recursos actual por separado.

Para obtener más información, consulte [Gestión del acceso a recursos](/docs/iam/mngiam.html#iammanidaccser).
