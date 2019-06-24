---

copyright:

  years: 2018, 2019
lastupdated: "2019-06-03"

keywords: organize resources, set up resource groups, best practice, resource group strategy

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Mejores prácticas para organizar los recursos en un grupo de recursos
{: #bp_resourcegroups}

Un grupo de recursos es una característica que puede utilizar para organizar los [recursos](/docs/resources?topic=resources-resource) de la cuenta para controlar el acceso y la facturación. Si está familiarizado con la utilización de espacios de Cloud Foundry, piense en organizar los recursos en grupos de recursos de forma similar a como ha organizado los recursos en espacios. Un recurso es cualquier cosa que se pueda crear, gestionar y contener dentro de un grupo de recursos. Los usuarios no se añaden a grupos de recursos. Solo pueden añadirse recursos.

Actualmente, no todos los servicios dan soporte al uso del control de acceso de {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) y de la asignación a un grupo de recursos. Los servicios habilitados para IAM le solicitan que asigne nuevas instancias de servicio a un grupo de recursos al crearlos desde el catálogo. Acceda a los recursos dentro de un grupo de recursos y el propio grupo de recursos lo gestionará IAM. Al utilizar roles de IAM, puede proporcionar a los usuarios acceso a los recursos organizados dentro de los grupos de recursos. Los roles de IAM también pueden proporcionar la capacidad de visualizar, editar, añadir nuevas instancias de servicio, o gestionar acceso a un grupo de recursos.

También puede encontrar la lista de servicios habilitados para IAM al asignar acceso a recursos desde la IU de Identidad y acceso realizando los siguientes pasos:
1. Vaya a **Gestionar** &gt; **Acceso (IAM)** y seleccione **Usuarios**.
2. Seleccione un usuario y pulse **Políticas de acceso**.
3. Seleccione **Asignar acceso** > **Asignar acceso a recursos**.
4. En el menú **Servicios**, seleccione el servicio que desea asignar. Para todos los servicios que aún no den soporte al uso de IAM, puede seguir utilizando organizaciones, espacios y roles de Cloud Foundry.
5. Pulse **Asignar**.

Las organizaciones, los espacios y los roles de Cloud Foundry están claramente separados de los grupos de recursos y de los roles de IAM. Un rol de Cloud Foundry nunca puede otorgar acceso a recursos dentro de un grupo de recursos.
{: note}


## Configuración de los grupos de recursos
{: #setuprgs}

Todos los usuarios obtienen un único grupo de recursos de forma predeterminada que se puede renombrar. Asigne el rol de editor o de administrador a todos los servicios de gestión de la cuenta para crear grupos de recursos. Si tiene una cuenta facturable, puede crear más de un grupo de recursos para organizar los recursos. Al organizar recursos en distintos grupos de recursos, puede:

* Hacer la asignación de acceso a un conjunto de recursos más sencilla utilizando un número mínimo de políticas
* Ver por información de uso de grupo de recursos para fines de facturación

Para crear un nuevo grupo de recursos, complete los siguientes pasos:

1. Vaya a **Gestionar** > **Cuenta**.
2. Amplíe los **Recursos de cuenta** y seleccione **Grupos de recursos**.
3. Pulse **Crear un grupo de recursos**.
4. Especifique un nombre para su grupo de recursos.
5. Pulse **Añadir**.

## Adición de recursos a un grupo de recursos
{: #addingtorgs}

Los servicios habilitados mediante el control de acceso de IAM pertenecen a un grupo de recursos en lugar de una organización o un espacio de Cloud Foundry. Cuando cree una instancia de servicio para uno de los servicios del catálogo, se le solicitará que asigne la instancia a un grupo de recursos.

La selección del grupo de recursos en el momento de crear la instancia es definitiva y no se puede cambiar.
{: important}

A medida que más servicios habiliten la asignación a grupos de recursos y el uso de control de acceso de IAM, se le notificará en la lista de recursos si dispone de instancias de servicios de Cloud Foundry existentes que sean elegibles para la migración. Al [migrar una instancia de servicio a un grupo de recursos](/docs/resources?topic=resources-migrate), estará creando una nueva instancia enlazada en un grupo de recursos de su elección y la instancia de Cloud Foundry se convertirá en un alias.


## Asignación de acceso a grupos de recursos y los recursos dentro de los mismos
{: #assigning_access_rgs}

Proporcione acceso para usuarios o grupos de usuarios organizados en grupos de acceso creando políticas de acceso. Las políticas de acceso establecen un objetivo, que es normalmente una instancia de servicio o todas las instancias de un servicio en un grupo de recursos, y un rol, que define el tipo de acceso permitido. Hay dos tipos de políticas de acceso que tienen que asignarse como propietario de cuenta para permitir que los usuarios de su cuenta accedan a trabajar con recursos en grupos de recursos:

* Acceso a recursos dentro de un grupo de recursos. Se puede otorgar acceso a todos los recursos de un grupo, o solo a servicios seleccionados dentro de un grupo.
* Acceso para permitir a los usuarios gestionar el grupo, lo que significa que los usuarios pueden ver el grupo, editar el nombre del grupo, gestionar el acceso para que terceros gestionen el grupo y, lo que es más importante, para poder crear y añadir nuevas instancias de servicio a un grupo.

Revise la tabla siguiente para obtener más información sobre los dos tipos de acceso y qué capacidad de hacer proporciona a un usuario cada rol de IAM de plataforma asignado:

|   | Acciones para acceder a la gestión de grupos de recursos | Acción en recursos en grupos de recursos |
|:-----------------|:--------------|:---------------|
| Rol Visor  | Ver el grupo y sus características, pero no los recursos del grupo | Ver recursos en el grupo |
| Rol Operador | No aplicable | No aplicable |
| Rol Editor | Ver o editar el nombre u otras características del grupo, pero no los recursos del grupo | Crear, suprimir, editar, suspender, reanudar, ver, enlazar y gestionar el acceso de recursos en el grupo de recursos |
| Rol Administrador |  Ver, editar o gestionar el acceso para el grupo, pero no los recursos del grupo | Crear, suprimir, editar, suspender, reanudar, ver, enlazar y gestionar el acceso de recursos en el grupo de recursos |
{: row-headers}
{: class="comparison-table"}
{: caption="Tabla 1. Acceso para grupos de recursos" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the selected role of an access policy. The column headers identify the type of policy whether its assigning access to manage a resource group or access to resources within a resource group. The remaining cells tell you the allowable actions based on the type of policy and the specific role that is selected as defined in the header rows."}

Si desea que un usuario pueda crear una nueva instancia de servicio y añadirla a un grupo de recursos, el usuario debe estar asignado como Visor o superior en el grupo de recursos y Editor o superior en el servicio.
{: tip}


## Políticas de acceso de ejemplo
{: #sample_policies}

Consulte las siguientes políticas de acceso de ejemplo para ayudarle a determinar cómo desea asignar acceso a recursos dentro de la cuenta que pertenece a los grupos de recursos.

1. Una política que otorga al usuario el Rol de plataforma “Administrador” en el Servicio de contenedor de {{site.data.keyword.Bluemix_notm}} en toda la cuenta. Una política con estos detalles permite al usuario acceder a todas las instancias de este servicio y permite al usuario crear instancias del servicio en cualquier grupo de recursos en el que el usuario tenga al menos rol de Visor. Los usuarios con el rol Administrador en cualquier recurso también pueden otorgar otros accesos de usuario a dicho recurso.
2. Una política que otorga al usuario el Rol de plataforma “Visor” en un grupo de recursos, pero no en sus recursos miembro. Una política con estos detalles permite la visibilidad de usuarios en el grupo de recursos, lo que es necesario para crear instancias de cualquier servicio en este grupo de recursos.
3. Una política que otorga al usuario el Rol de plataforma “Editor” en todos los recursos del grupo de recursos. Un usuario con el rol Editor en un recurso puede editar o suprimir dicho recurso.
4. Una política que otorga al usuario el Rol de plataforma “Administrador” en toda la cuenta (todos los servicios habilitados por IAM). Una política con estos detalles permite al usuario realizar cualquier acción de plataforma en cualquier recurso de toda la cuenta y también incluye la capacidad de realizar acciones de gestión en la cuenta, con la gestión de los grupos de recursos en la cuenta.

## Ejemplos de casos de uso
{: #usecase_examples}

Para cada uno de estos casos de uso, si tiene un grupo de usuarios que desea que tengan todos el mismo nivel de acceso, añádalos a un [grupo de acceso](/docs/iam?topic=iam-groups). Al utilizar grupos de acceso, puede utilizar un número mínimo de políticas de acceso, ya que todos los miembros del grupo de acceso heredan cualquier acceso asignado al grupo.
{: tip}

<ol>
<li><p>Tengo una cuenta pequeña con solo 10 usuarios que trabajan todos juntos en un único proyecto. Algunos de estos usuarios deben gestionar la cuenta y asignar acceso a otros usuarios. Algunos de los usuarios necesitan suministrar instancias de servicio que incurrirán en gastos. Otros usuarios son desarrolladores de aplicaciones que solo necesitan utilizar las instancias de servicio desde los componentes de su aplicación.</p>
<p>Todos estos usuarios deben tener varios roles en la cuenta y el grupo de recursos predeterminado. No hay necesidad de crear grupos de recursos adicionales para separar recursos o restringir a algunos usuarios de acceder a algunos de los recursos. A los usuarios se les puede otorgar los roles en la cuenta y en el grupo de recursos predeterminado que sean apropiados a sus necesidades: Administrador de la cuenta para los usuarios que necesitan gestionar la cuenta y dar acceso a terceros, Editor del grupo de recursos predeterminado y sus miembros para usuarios que necesitan suministrar instancias de servicio, y Lector o Escritor de los miembros del grupo de recursos para usuarios que solo necesitan utilizar las instancias de servicio.</p>
</li>
<li><p>Tengo una cuenta que incluye tres equipos distintos que trabajan en tres proyectos. Algunos usuarios son administradores y necesitan la capacidad de crear nuevos grupos de recursos y asignar acceso a los usuarios a grupos de recursos. Los usuarios restantes solo necesitan acceso al grupo de recursos asociado con su proyecto.</p>
<p>Quiero asignar a los administradores el rol de Administrador en todos los servicios habilitados para IAM. Quiero asignar a los usuarios restantes varios roles sobre el grupo de recursos y los miembros de grupo de recursos asociados con su proyecto: Editor de grupo de recursos para aquellos que necesiten crear instancias, más Lector o Escritor de miembro de grupo de recursos para aquellos que necesiten utilizar instancias.</p>
</li>
<li><p>Tengo una cuenta con varios grupos de recursos. Tengo algunos usuarios que son los administradores para el Servicio A de toda mi cuenta y necesito acceso a todas las instancias de dicho servicio, además de la capacidad de crear instancias, pero estos usuarios no necesitan acceso a ningún otro recurso de la cuenta.</p>
<p>Quiero asignar a estos usuarios el rol Administrador en el Servicio A a nivel de cuenta, así como asignarles el rol Visor para todos los grupos de recursos de la cuenta donde necesiten crear instancias.</p>
</li>
<li><p>Tengo un usuario en mi cuenta que solo necesita acceso a un recurso específico en un servicio, por ejemplo la capacidad de escribir en un Grupo A en IBM Cloud Object Storage. Este usuario no debería ver los grupos de recursos en mi cuenta ni acceder a ningún otro servicio ni a ningún otro grupo en esta instancia de Cloud Object Storage.</p>
<p>Quiero dar a este usuario el rol Escritor en el Grupo A en la instancia específica de Cloud Object Storage. Puede otorgar esta política utilizando interfaces específicas del servicio (la IU de Cloud Object Storage, en este ejemplo) o la IU principal de Asignar acceso. La IU específica del servicio está recomendada porque le permite elegir entre una lista de recursos, mientras que la IU de Asignar acceso no muestra recursos más allá del nivel de instancia de servicio y deberá especificar manualmente el CRN para asignar la política a estos recursos.</p>
</li>
<li><p>Hoy estoy utilizando las organizaciones y los espacios de Cloud Foundry, pero voy a empezar a utilizar grupos de recursos y grupos de acceso para mis servicios habilitados para IAM. Actualmente, mis usuarios y recursos están organizados en organizaciones para las líneas de negocio y los espacios se utilizan para diferentes proyectos dentro de una línea de negocio.</p>
<p>Utilizaré grupos de recursos para organizar recursos de la misma forma en que lo hice con espacios, pensando en cada grupo de recursos como un espacio de proyectos. A continuación, configuraré grupos de acceso independientes para dar el acceso necesario a mis usuarios para los grupos de recursos de nivel de proyecto adecuados. El acceso se puede dar a todos los recursos de un grupo de recursos o incluso a un grupo de recursos selecto dentro de un grupo de recursos. Por lo tanto, puede configurar cada grupo de acceso con distintos niveles de acceso a los recursos dentro de un grupo de recursos, lo que otorga a cada grupo de usuarios el acceso que necesitan para trabajar con los recursos o el propio grupo de recursos.</p>
</li>
</ol>
