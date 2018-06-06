---

copyright:
  years: 2015, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}

# Utilización de servicios en otra región
{: #cross_region_service}

Si tiene una instancia de servicio creada y enlazada a apps en una región, puede utilizar eta instancia de servicio en otra región mediante uno de los métodos siguientes:
{: shortdesc}

  * Utilice las credenciales del servicio para configurar directamente su instancia de app. Consulte [Habilitación de apps externas para utilizar el servicio de {{site.data.keyword.Bluemix_notm}}](/docs/apps/reqnsi.html#accser_external){: new_window} para obtener detalles.
  * Crear un servicio proporcionado por el usuario como un puente.

	Para utilizar una instancia de servicio existente en otra región, siga estos pasos:

      1. Vaya a la región en la que reside la instancia de servicio. En la barra de menús de {{site.data.keyword.Bluemix_notm}}, expanda el menú **Región** y seleccione la región en la que reside la instancia de servicio.

      2. Recupere las credenciales y los parámetros de conexión de la variable de entorno VCAP_SERVICES de la instancia de servicio de la región en la que existe el servicio. Siga estos pasos:

	       1. En el Panel de control de {{site.data.keyword.Bluemix_notm}}, pulse el mosaico de la aplicación. Se muestra la página Visión general.
	       2. En el panel de navegación, pulse **Credenciales**. Se muestran los detalles de la variable de entorno *VCAP_SERVICES*. Registre el contenido JSON correspondiente a la instancia de servicio.

      3. Vaya a la región en la que desea utilizar la instancia de servicio. En la barra de menús de {{site.data.keyword.Bluemix_notm}}, expanda el menú **Región** y seleccione la región en la que desea utilizar la instancia de servicio.

      4. Cree una instancia de servicio suministrada por el usuario utilizando las credenciales y los parámetros de conexión que ha registrado de la variable de entorno *VCAP_SERVICES*. Para obtener información sobre cómo crear una instancia de servicio proporcionada por el usuario, consulte el tema sobre [creación de una instancia de servicio proporcionada por el usuario](/docs/apps/reqnsi.html#user_provide_services).

      5. Enlace la instancia de servicio proporcionada por el usuario a la app con el siguiente mandato:

	     ```
	     bluemix service bind myapp user-provided_service_instance
	     ```
