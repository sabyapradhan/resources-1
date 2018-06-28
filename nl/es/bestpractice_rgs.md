---

copyright:

  years: 2018
lastupdated: "2018-06-08"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}


# Mejores prácticas para organizar los recursos en un grupo de recursos
{: #bp_resourcegroups}

Los grupos de recursos son una característica para organizar los [recursos](/docs/resources/acct_resources.html#resource) de su cuenta para finalidades de control de acceso y de facturación. Si está familiarizado con la utilización de espacios de Cloud Foundry, puede pensar en organizar recursos en grupos de recursos de forma similar a la forma en la que ha organizado recursos en espacios. Un recurso es cualquier cosa que se pueda crear, gestionar y contener dentro de un grupo de recursos. Los usuarios no se añaden a grupos de recursos. Solo pueden añadirse recursos. 

Actualmente, no todos los servicios dan soporte al uso del control de acceso de {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) y de la asignación a un grupo de recursos. Los servicios gestionados por IAM le solicitan que asigne nuevas instancias de servicio a un grupo de recursos al crearlos desde el catálogo. Acceda a los recursos dentro de un grupo de recursos y el propio grupo de recursos lo gestionará IAM. Al utilizar roles de IAM, puede proporcionar a los usuarios acceso a los recursos organizados dentro de los grupos de recursos. Los roles de IAM también pueden proporcionar la capacidad de visualizar, editar, añadir nuevas instancias de servicio, o gestionar acceso a un grupo de recursos.

También puede encontrar la lista de servicios gestionados por IAM al asignar acceso a recursos desde la IU de Identidad y acceso. Vaya a **Gestionar** &gt; **Seguridad** &gt; **Identidad y acceso**, a continuación seleccione cualquier usuario o ID de servicio y seleccione **Asignar acceso** desde el menú **Acciones**. A continuación, seleccione **Asignar acceso a recursos** y, en el menú desplegable **Servicios**, puede ver los servicios que soporta utilizando IAM. Para todos los servicios que no soportan aún el uso de IAM, puede seguir utilizando organizaciones, espacios y roles de Cloud Foundry. 

Las organizaciones, los espacios y los roles de Cloud Foundry están claramente separados de los grupos de recursos y de los roles de IAM. Por lo tanto, un rol de Cloud Foundry nunca puede otorgar acceso a recursos dentro de un grupo de recursos. 
{: tip}


## Configuración de los grupos de recursos

Todos los usuarios obtienen un único grupo de recursos de forma predeterminada que se puede renombrar. Si tiene una cuenta facturable, puede crear más de un grupo de recursos para organizar los recursos. Al organizar recursos en distintos grupos de recursos, puede:

* Hacer la asignación de acceso a un conjunto de recursos más sencilla utilizando un número mínimo de políticas 
* Ver por información de uso de grupo de recursos para fines de facturación 

Para crear un nuevo grupo de recursos, complete los siguientes pasos:

1. Vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos**.
2. Pulse **Crear un grupo de recursos**.
3. Especifique un nombre para su grupo de recursos.
4. Pulse **Añadir**.


## Adición de recursos a un grupo de recursos

Los servicios gestionados mediante el control de acceso de IAM pertenecen a un grupo de recursos en lugar de una organización o un espacio de Cloud Foundry. Cuando cree una instancia de servicio para uno de los servicios del catálogo, se le solicitará que asigne la instancia a un grupo de recursos. 

**Importante**: La selección del grupo de recursos en el momento de crear la instancia es final y no se puede cambiar.

A medida que más servicios habiliten la asignación a grupos de recursos y el uso de control de acceso de IAM, se le notificará en el panel de control si dispone de instancias de servicios de Cloud Foundry existentes que sean elegibles para la migración. Al [migrar una instancia de servicio a un grupo de recursos](/docs/resources/instance_migration.html), estará creando una nueva instancia enlazada en un grupo de recursos de su elección y la instancia de Cloud Foundry se convertirá en un alias. 


## Asignación de acceso a grupos de recursos y los recursos dentro de los mismos

Proporcione acceso para usuarios o grupos de usuarios organizados en grupos de acceso creando políticas de acceso. Las políticas de acceso establecen un objetivo, que es normalmente una instancia de servicio o todas las instancias de un servicio en un grupo de recursos, y un rol, que define el tipo de acceso permitido. Hay dos tipos de políticas de acceso que tienen que asignarse como propietario de cuenta para permitir que los usuarios de su cuenta accedan a trabajar con recursos en grupos de recursos:

* Acceso a recursos dentro de un grupo de recursos. Se puede otorgar acceso a todos los recursos de un grupo, o solo a servicios seleccionados dentro de un grupo.
* Acceso para permitir a los usuarios gestionar el grupo, lo que significa que los usuarios pueden ver el grupo, editar el nombre del grupo, gestionar el acceso para que terceros gestionen el grupo y, lo que es más importante, poder crear y añadir nuevas instancias de servicio a un grupo.

Revise la tabla siguiente para obtener más información sobre los dos tipos de acceso y qué capacidad de hacer proporciona a un usuario cada rol de IAM de plataforma asignado:

| Detalles de política de acceso  | Acciones para acceder en grupos de recursos | Acción en recursos en grupos de recursos | 
|:-----------------|:--------------|:---------------|
| Asignar acceso a | Grupo de recursos seleccionado | Servicio seleccionado en un grupo de recursos |
| Rol Visor  | Ver el grupo y sus características, pero no los recursos del grupo | Ver recursos en el grupo | 
| Rol Operador | No aplicable | No aplicable | 
| Rol Editor | Ver o editar el nombre u otras características del grupo, pero no los recursos del grupo | Crear, suprimir, editar, suspender, reanudar, ver, enlazar y gestionar el acceso de recursos en el grupo de recursos |
| Rol Administrador |  Ver, editar o gestionar el acceso para el grupo, pero no los recursos del grupo | Crear, suprimir, editar, suspender, reanudar, ver, enlazar y gestionar el acceso de recursos en el grupo de recursos | 
{: caption="Tabla 1. Acceso para grupos de recursos" caption-side="top"}

Si desea que un usuario pueda crear una nueva instancia de servicio y añadirla a un grupo de recursos, el usuario debe estar asignado como Visor o superior en el grupo de recursos y Editor o superior en el servicio.
{: tip}


## Políticas de acceso de ejemplo

Consulte las siguientes políticas de acceso de ejemplo para ayudarle a determinar cómo desea asignar acceso a recursos dentro de la cuenta que pertenece a los grupos de recursos.

1. Una política que otorga al usuario el Rol de plataforma “Administrador” en el Servicio de contenedor de {{site.data.keyword.Bluemix_notm}} en toda la cuenta. Una política con estos detalles permite al usuario acceder a todas las instancias de este servicio y permite al usuario crear instancias del servicio en cualquier grupo de recursos en el que el usuario tenga al menos rol de Visor. Los usuarios con el rol Administrador en cualquier recurso también pueden otorgar otros accesos de usuario a dicho recurso.
2. Una política que otorga al usuario el Rol de plataforma “Visor” en un grupo de recursos, pero no en sus recursos miembro. Una política con estos detalles permite la visibilidad de usuarios en el grupo de recursos, lo que es necesario para crear instancias de cualquier servicio en este grupo de recursos.
3. Una política que otorga al usuario el Rol de plataforma “Editor” en todos los recursos del grupo de recursos. Un usuario con el rol Editor en un recurso puede editar o suprimir dicho recurso.
4. Una política que otorga al usuario el Rol de plataforma “Administrador” en toda la cuenta (todos los servicios habilitados por IAM). Una política con estos detalles permite al usuario realizar cualquier acción de plataforma en cualquier recurso de toda la cuenta y también incluye la capacidad de realizar acciones de gestión en la cuenta, con la gestión de los grupos de recursos en la cuenta.

## Ejemplos de casos de uso

Para cada uno de estos casos de uso, si tiene un grupo de usuarios que desea que tengan todos el mismo nivel de acceso, añádalos a un [grupo de acceso](/docs/iam/groups.html#groups). Al utilizar grupos de acceso, puede utilizar un número mínimo de políticas de acceso, ya que todos los miembros del grupo de acceso heredan el acceso asignado al grupo.
{: tip}

1. Tengo una cuenta pequeña con solo 10 usuarios que trabajan todos juntos en un único proyecto. Algunos de estos usuarios deben poder gestionar la cuenta y asignar acceso a otros usuarios. Algunos de los usuarios necesitan poder suministrar instancias de servicio que incurrirán en gastos. Otros usuarios son desarrolladores de aplicaciones que solo necesitan poder utilizar las instancias de servicio desde los componentes de su aplicación. Todos estos usuarios deben tener varios roles en la cuenta y el grupo de recursos predeterminado. No hay necesidad de crear grupos de recursos adicionales para separar recursos o restringir a algunos usuarios de acceder a algunos de los recursos. A los usuarios se les puede otorgar los roles en la cuenta y en el grupo de recursos predeterminado que sean apropiados a sus necesidades. Administrador de la cuenta para los usuarios que necesitan poder gestionar la cuenta y dar acceso a terceros, Editor del grupo de recursos predeterminado y sus miembros para usuarios que necesitan poder suministrar instancias de servicio, y Lector o Escritor de los miembros del grupo de recursos para usuarios que solo necesitan utilizar las instancias de servicio.
2. Tengo una cuenta que incluye tres equipos distintos que trabajan en tres proyectos. Algunos usuarios son administradores y necesitan la capacidad de añadir nuevos usuarios a la cuenta, crear nuevos grupos de recursos y asignar acceso a los usuarios a grupos de recursos. Los usuarios restantes solo necesitan acceso al grupo de recursos asociado con su proyecto. Quiero asignar a la cuenta de administradores el rol de Administrador. Quiero asignar a los usuarios restantes varios roles al grupo de recursos y a los miembros de grupo de recursos asociados con su proyecto. Editor de grupo de recursos para aquellos que necesiten crear instancias, más Lector o Escritor de miembro de grupo de recursos para aquellos que necesiten poder utilizar instancias.
3. Tengo una cuenta con varios grupos de recursos. Tengo algunos usuarios que son los administradores para el Servicio A de toda mi cuenta y necesito acceso a todas las instancias de dicho servicio, además de la capacidad de crear instancias, pero estos usuarios no necesitan acceso a ningún otro recurso de la cuenta. Quiero asignar a estos usuarios el rol Administrador en el Servicio A a nivel de cuenta, así como asignarles el rol Visor para todos los grupos de recursos de la cuenta donde necesiten poder crear instancias.
4. Tengo un usuario en mi cuenta que solo necesita acceso a un recurso específico en un servicio, por ejemplo la capacidad de escribir en un Grupo A en IBM Cloud Object Storage. Este usuario no debería poder ver los grupos de recursos en mi cuenta ni acceder a ningún otro servicio ni a ningún otro grupo en esta instancia de Cloud Object Storage. Quiero dar a este usuario el rol Escritor en el Grupo A en la instancia específica de Cloud Object Storage. Puede otorgar esta política utilizando interfaces específicas del servicio (la IU de Cloud Object Storage, en este ejemplo) o la IU principal de Asignar acceso. La IU específica del servicio está recomendada porque le permitirá elegir entre una lista de recursos, mientras que la IU de Asignar acceso no muestra recursos por debajo del nivel de instancia de servicio y deberá especificar manualmente el CRN para asignar la política a estos recursos.
