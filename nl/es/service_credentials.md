---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}


# Adición de una credencial
{: #service_credentials}

Puede generar un nuevo conjunto de credenciales para casos en los que quiera conectarse manualmente un consumidor externo a un servicio de {{site.data.keyword.Bluemix}}. Por ejemplo, si está intentando enlazar una app de AWS a un servicio Watson, necesita generar una nueva credencial que se pueda utilizar para enlazarlos.

## Adición de una credencial al enlazar un servicio habilitado para IAM
{: #IAM}

Los servicios gestionados por la Gestión de identidad y acceso de {{site.data.keyword.Bluemix_notm}} (IAM) pueden generar una clave de recurso, también conocida como credencial. Las credenciales son específicas del servicio y varían en función de cómo define cada servicio las credenciales que necesita generar. Una credencial puede contener un nombre de usuario, una contraseña, un nombre de host, un puerto y una URL.

Sin embargo, el contenido de cada credencial es exclusivo para el servicio que la genera, todos los servicios gestionados por IAM requieren esas nuevas credenciales incluidas en un rol de acceso de servicio de IAM. Algunos servicios pueden generar más datos que requieren que se pasen parámetros. Por ejemplo, un servicio puede necesitar que especifique un parámetro de idioma para establecer el idioma predeterminado devuelto en la clave de recurso que se genera.

Complete los siguientes pasos para añadir una credencial a un servicio gestionado por IAM:

1. Desde la lista de recursos, seleccione el nombre del servicio para abrir la página de detalles del servicio. A continuación, seleccione el separador Credenciales y pulse **Credencial nueva +**.
2. En el diálogo Añadir credencial nueva, proporcione un **Nombre**.
3. Especifique el rol. Este valor define el rol de acceso de servicio de IAM. Para obtener más información, consulte: [Acceso de IAM](/docs/iam/users_roles.html#userroles)
4. Opcionalmente, puede proporcionar un ID de servicio permitiendo a IAM generar un valor exclusivo para usted o proporcionando un ID de servicio existente. Para obtener más información, consulte: [Creación y gestión de ID de servicio](/docs/iam/serviceid.html#serviceids)
5. Opcionalmente, puede proporcionar más parámetros como objeto JSON válido que contiene parámetros de configuración específicos del servicio, proporcionados en línea o en un archivo.

  La mayoría de los servicios no requieren parámetros adicionales, y para los servicios que sí los requieren, cada servicio define su propia lista exclusiva de parámetros. Para obtener una lista de parámetros de configuración soportados, consulte la documentación para ver la oferta de servicios concreta.
  {: note}
6. Pulse **Añadir** para generar la nueva credencial de servicio.

## Adición de una credencial al enlazar un servicio de Cloud Foundry
{: #cf}

Los servicios de Cloud Foundry pueden generar una clave de servicio, también conocida como credencial. Las credenciales son específicas del servicio y varían en función de cómo define cada servicio las credenciales que necesita generar. Una credencial de servicio puede contener un nombre de usuario, una contraseña, un nombre de host, un puerto y una URL.

Sin embargo, el contenido de cada credencial es exclusivo para el servicio que la genera. Algunos servicios pueden generar datos adicionales que requieren que se pasen parámetros. Por ejemplo, un servicio puede necesitar que especifique un parámetro de idioma para establecer el idioma predeterminado devuelto en la clave de servicio que se genera.

Siga estos pasos para añadir una credencial de Cloud Foundry:

1. En la página de detalles de servicio, seleccione el separador Credenciales y pulse **Credencial nueva +**.
2. En el diálogo Añadir credencial nueva, proporcione un **Nombre**.
3. Opcionalmente, puede proporcionar más parámetros como objeto JSON válido que contiene parámetros de configuración específicos del servicio, proporcionados en línea o en un archivo.

  La mayoría de los servicios no requieren parámetros adicionales, y para los servicios que sí los requieren, cada servicio define su propia lista exclusiva de parámetros. Para obtener una lista de parámetros de configuración soportados, consulte la documentación para ver la oferta de servicios concreta.
  {: note}
4. Pulse **Añadir** para generar la nueva credencial de servicio.

