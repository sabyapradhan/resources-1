---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-06"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Conexión de servicios a una app de Cloud Foundry
{: #s2s_binding}

Para utilizar un servicio en una app de Cloud Foundry, debe crear una conexión o enlazar ese servicio a la app.
{: shortdesc}

Para conectar un servicio a la app empezando desde la página de detalles de un servicio específico, siga los pasos siguientes:

También puede crear conexiones entre la app y al servicio. Seleccione la app en la lista de recursos, vaya al menú **Conexiones** y seleccione el servicio.
{: note}

1. En la lista de recursos, pulse **Servicios** y seleccione el servicio al que desea acceder. Se mostrará la página de detalles del servicio.
2. Pulse **Conexiones** en el área de navegación.
3. Pulse **Crear conexión**.
4. Pulse **Conectar** para la fila de la app para la que desea crear la conexión.
5. Seleccione un rol de acceso para asignarlo a la conexión. Este rol define las acciones permitidas que puede llevar a cabo la app que accede al servicio.
6. Opcional: seleccione, cree o genere automáticamente un ID de servicio que utilizará la app para acceder al servicio. A este ID de servicio se le asigna el rol de acceso que ha seleccionado en el paso anterior y, si no ha seleccionado ninguna opción, se genera una.
7. Opcional: añada parámetros de configuración en formato JSON.
8. Pulse **Conectar y volver transferir app**.


Si desea restringir el acceso de una app a la instancia de servicio, pulse **Conexiones** en el panel de navegación y luego pulse **Desenlazar** en el menú de la aplicación conectada para eliminar el enlace de servicio.
{: tip}
