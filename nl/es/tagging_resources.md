---

copyright:

  years: 2018,2019
lastupdated: "2019-01-29"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Cómo trabajar con etiquetas
{: #tag}

El usuario asigna una etiqueta a un recurso para filtrar fácilmente los recursos en la lista de recursos. Puede utilizar etiquetas para organizar sus recursos y encontrarlos fácilmente más adelante.  
{: shortdesc}

Para ver una lista completa de las etiquetas de su cuenta, vaya a **Gestionar > Cuenta** y seleccione **Etiquetas**.

## Reglas de etiquetado y limitaciones
{: #limits}

El tamaño máximo de una etiqueta es de 128 caracteres. Los caracteres permitidos son A-Z, 0-9, espacios en blanco, signo de subrayado, guion, punto y signo de dos puntos, y las etiquetas no distinguen entre mayúsculas y minúsculas. El signo de dos puntos convierte la etiqueta en una serie en la que puede aislar dos partes lógicas, como un par `clave:valor`. No puede utilizar un signo de dos puntos en una etiqueta sin crear este emparejamiento. Una coma separa etiquetas y no se pueden utilizar en el nombre de la propia etiqueta.


## Adición y eliminación de etiquetas en un recurso
{: #add-remove}

1. En la consola de {{site.data.keyword.Bluemix_notm}}, pulse el icono de Menú ![Icono de Menú](../icons/icon_hamburger.svg) > **Lista de recursos** para ver su lista de recursos. 
2. Expanda el triángulo del tipo de recurso que contiene el recurso que desea etiquetar. Por ejemplo, si desea etiquetar una instancia de {{site.data.keyword.cos_full_notm}}, expanda **Almacenamiento**.  
3. Pulse el icono Acciones ![Icono Acciones](../icons/action-menu-icon.svg) para añadir o actualizar una etiqueta correspondiente al recurso. 

    * Para añadir una etiqueta, pulse el menú Acciones ![Icono de Acciones](../icons/action-menu-icon.svg), seleccione **Añadir etiquetas** y escriba un nombre para la etiqueta. 
    * Para añadir etiquetas adicionales, pulse el icono Editar ![Icono Editar](../icons/edit-tagging.svg) situado junto a la etiqueta visualizada y escriba un nombre para la etiqueta. Pulse Intro para seguir añadiendo etiquetas.
4. Para eliminar una etiqueta, pulse el icono Editar ![Icono Editar](../icons/edit-tagging.svg). A continuación, pulse el icono Eliminar ![Icono Eliminar](../icons/close-tagging.svg) junto a la etiqueta. 

## Búsqueda de etiquetas
{: #search-tags}

Puede buscar etiquetas utilizando cualquiera de los métodos siguientes:

  * Pruebe la barra de búsqueda que se encuentra en la barra de menús de la consola de {{site.data.keyword.Bluemix_notm}}.
  * Puede filtrar la lista de recursos por la etiqueta que está buscando.
  * En la página de detalles de la aplicación, puede localizar las etiquetas que están asociadas con dicho recurso.

La misma etiqueta se puede adjuntar a varios recursos por parte de distintos usuarios en la misma cuenta de facturación, y no todos los usuarios tienen visibilidad sobre todos los recursos de la cuenta.
{: note}


## Etiquetado para distribuidores
{: #resell}

Las etiquetas son visibles para todos los miembros de una cuenta.
Si su cuenta está asociada con diferentes organizaciones, por ejemplo si es un distribuidor, quizás desee recomendar a sus clientes que no almacenen en etiquetas información que pueda revelar información confidencial a terceros en la misma cuenta.

Para controlar la visibilidad de las etiquetas, haga circular las directrices de etiquetado y comunique a los usuarios que las etiquetas son visibles en toda la cuenta. 

Utilice códigos en lugar de nombres para clientes y cuentas y evite colocar información confidencial en etiquetas.
{: tip}

