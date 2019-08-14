---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Acceso seguro a servicios utilizando puntos finales de servicio
{: #service-endpoints}

Los clientes que utilizan servicios basados en la nube para cargas de trabajo de producción ponen cada vez más énfasis en la seguridad. Para muchos clientes, el acceso a los servicios de forma segura no es solo una política corporativa razonable, sino que en algunos casos es una exigencia legal de obligado cumplimiento. {{site.data.keyword.IBM_notm}} ha mejorado las opciones de conectividad para los clientes que necesitan opciones de conectividad aislada para sus cargas de trabajo. 

Con los puntos finales de servicio de {{site.data.keyword.cloud}}, puede conectarse a los servicios de {{site.data.keyword.cloud_notm}} a través de la red privada de {{site.data.keyword.cloud_notm}}. El traslado de estas cargas de trabajo de la red pública ofrece dos ventajas:

* Los servicios ya no se sirven en una dirección IP direccionable a Internet. Cada vez resulta más común que los consumidores de la nube quieran tener acceso limitado, o incluso ningún acceso, a Internet público desde cualquiera de sus servicios. Ahora, con la característica de punto final de servicio, los equipos de servicio pueden crear una interfaz sobre la red privada para el servicio que los clientes pueden utilizar para conectarse. El acceso a Internet ya no es un requisito para que se conecte a los servicios de {{site.data.keyword.cloud_notm}}.
* No hay cargos de ancho de banda facturable ni por uso de la red privada. Anteriormente, se le facturaba por el ancho de banda de salida cuando se conectaba a un servicio de {{site.data.keyword.cloud_notm}}. 

En la siguiente figura se muestra cómo se direcciona el tráfico a través de la red privada de {{site.data.keyword.cloud_notm}} cuando se accede a los servicios de la nube a través de puntos finales de servicio:

![Punto final de servicio de IBM Cloud](images/CSE.png "Tráfico que se direcciona a través de un punto final de servicio")

Para utilizar los puntos finales de servicio de {{site.data.keyword.cloud_notm}}, debe habilitar el direccionamiento y el reenvío virtuales (VRF) en su cuenta.  A continuación, puede habilitar el uso de puntos finales de servicio. Una vez que ambas opciones están habilitadas, puede empezar a crear servicios que den soporte al uso de VRF y de puntos finales de servicio desde el catálogo. Para obtener más información, consulte [Habilitación de VRF y puntos finales de servicio](/docs/account?topic=account-vrf-service-endpoint).
