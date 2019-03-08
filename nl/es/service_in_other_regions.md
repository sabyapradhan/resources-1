---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# Utilización de servicios en otra región
{: #cross_region_service}

Si tiene una instancia de servicio creada y enlazada a apps en una región, puede utilizar esta instancia de servicio en otra región mediante uno de los métodos siguientes:
{: shortdesc}

  * Utilice las credenciales del servicio para configurar directamente su instancia de app. Consulte [Conexión de servicios a apps externas](/docs/resources?topic=resources-externalapp#externalapp) para ver más detalles.
  * Crear un servicio proporcionado por el usuario como un puente.

	Para utilizar una instancia de servicio existente en otra región, siga estos pasos:

      1. Para cambiar a la región en la que se encuentra la instancia de servicio, pulse el **icono Menú ![Icono Menú](../icons/icon_hamburger.svg)** > **Lista de recursos**. Luego amplíe el menú **UBICACIÓN** y seleccione la región.

      2. Recupere las credenciales y los parámetros de conexión de la variable de entorno VCAP_SERVICES de la instancia de servicio de la región en la que existe el servicio. Siga estos pasos:

	       1. En el panel de control de {{site.data.keyword.Bluemix_notm}}, pulse **Ver todo** en el mosaico de apps. Se muestra la página Visión general.
	       2. En el panel de navegación, pulse **Credenciales**. Se muestran los detalles de la variable de entorno *VCAP_SERVICES*. Registre el contenido JSON correspondiente a la instancia de servicio.

      3. Vaya a la región en la que desea utilizar la instancia de servicio. Pulse el **icono Menú ![Icono Menú](../icons/icon_hamburger.svg)** > **Lista de recursos**. Luego expanda el menú **UBICACIÓN** y seleccione la región donde desea utilizar la instancia de servicio.

      4. Cree una instancia de servicio suministrada por el usuario utilizando las credenciales y los parámetros de conexión que ha registrado de la variable de entorno *VCAP_SERVICES*.

      5. Enlace la instancia de servicio proporcionada por el usuario a la app con el siguiente mandato:

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
