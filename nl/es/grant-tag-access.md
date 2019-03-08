---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: resources

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Cómo otorgar a los usuarios acceso a recursos de etiqueta
{: #access}

Como propietario de la cuenta, quizás desee delegar algunas de las responsabilidades en cuanto a etiquetado de recursos. Para ello, puede otorgar acceso a otros usuarios de la cuenta para añadir y eliminar etiquetas de recursos. Para que los usuarios de una cuenta puedan añadir etiquetas a un recurso, deben tener asignado el acceso adecuado. El acceso a los servicios pertenecientes a un grupo de recursos se gestiona mediante políticas de acceso de {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) y el acceso a los servicios pertenecientes a una organización y espacio de Cloud Foundry se gestiona mediante roles de organización y espacio de Cloud Foundry.
{: shortdesc}

## Permisos de etiquetado
{: #tagging-permissions}

Las etiquetas son visibles para todos los usuarios de una cuenta. Una vez se ha etiquetado un recurso, la etiqueta resulta visible para todos los usuarios que tienen acceso de lectura al recurso. Para añadir o eliminar una etiqueta de un recurso, se necesitan ciertos roles o permisos que dependen del tipo de recurso. Consulte la siguiente tabla para ver el rol necesario para cada tipo de recurso.


| Tipo de recurso | Rol |
|--------|---------------|
| Habilitado para IAM | Editor o Administrador sobre el recurso |
| Cloud Foundry | Rol de Desarrollador sobre el espacio al que pertenece el recurso  |
| Infraestructura clásica*| Permiso para ver detalles de hardware o permiso para ver detalles del servidor virtual |
| Cloud Object Storage S3 en la infraestructura clásica | Permiso para gestionar el almacenamiento |
{: caption="Tabla 1. roles necesarios para añadir y eliminar etiquetas" caption-side="top"}

*Los recursos que se pueden etiquetar en la infraestructura clásica son Invitado virtual, Host dedicado virtual, Controlador de distribución de aplicación de red, Miembro de pasarela, Subred, VLAN y Cortafuegos de VLAN (dedicado).


## Cómo otorgar acceso para etiquetar recursos habilitados para IAM
{: #iam-managed}

Los recursos pertenecientes a un grupo de recursos se gestionan mediante políticas de acceso de {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Siga los pasos siguientes para asignar el rol de Editor a un usuario para que pueda etiquetar recursos habilitados para IAM:

  1. En la consola de {{site.data.keyword.Bluemix_notm}}, pulse **Gestionar > Acceso (IAM)** y seleccione **Usuarios**.
  2. Pulse el nombre del usuario al que va a otorgar acceso.
  3. Pulse **Políticas de acceso** > **Asignar acceso**.
  4. Seleccione la opción **Asignar acceso a recursos**.
  5. En la lista de servicios, seleccione un servicio específico o seleccione **Todos los servicios habilitados para identidad y acceso**.
  6. En la lista de roles de acceso de la plataforma, seleccione **Editor**.
  7. Pulse **Asignar**.

## Cómo otorgar acceso para etiquetar recursos de Cloud Foundry
{: #cf_tag_access}

Los recursos pertenecientes a una organización y espacio de Cloud se gestionan mediante roles de organización y espacio de Cloud Foundry. Siga los pasos siguientes para asignar el rol de espacio de Desarrollador para que un usuario pueda etiquetar recursos de Cloud Foundry:

 1. Pulse **Gestionar > Acceso (IAM)** y seleccione **Usuarios**.
2. Seleccione el nombre del usuario al que desea asignar el acceso.
3. Pulse **Acceso de Cloud Foundry**.
4. Pulse **Asignar organización**.
5. Expanda y seleccione la `Organización` con la instancia de servicio sobre la que desea otorgar acceso al usuario.
6. Seleccione la región.
7. Seleccione el rol de espacio **Desarrollador**.
8. Pulse **Guardar rol**.

## Cómo otorgar acceso para etiquetar recursos de la infraestructura clásica
{: #classic-infra}

Siga los pasos siguientes para asignar el rol de acceso de servicio de Gestor para que un usuario pueda etiquetar servicios de la infraestructura clásica:

  1. Pulse **Gestionar > Acceso (IAM)** y seleccione **Usuarios**.
  2. Pulse el nombre del usuario al que va a otorgar acceso.
  3. Pulse **Infraestructura clásica**
  4. En el separador **Permisos**, expanda la categoría **Dispositivos**.
  5. Seleccione **Ver detalles de hardware** y **Ver detalles de servidor virtual**. Si tiene que asignar acceso a Cloud Object Storage S3, asigne el permiso **Gestión de almacenamiento**.
  6. Pulse **Guardar**.
  7. Pulse el separador **Dispositivos**.
  8. Seleccione **Todos los servidores nativos** o **Todos los servidores virtuales** en función del recurso que desee etiquetar.
