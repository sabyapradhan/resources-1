---

copyright:

  years: 2015, 2019
lastupdated: "2019-05-08"

keywords: service key, api key, bind, credential

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}
{:tip: .tip}


# Adición y visualización de credenciales
{: #service_credentials}

Puede generar un nuevo conjunto de credenciales para casos en los que quiera conectarse manualmente una app o un consumidor externo a un servicio de {{site.data.keyword.Bluemix}}. Por ejemplo, si está intentando enlazar una app de AWS a un servicio Watson, necesita generar una nueva credencial que se pueda utilizar para enlazarlos. Una vez que se haya creado la credencial, puede
[añadirla manualmente](/docs/apps/tutorials?topic=creating-apps-credentials_overview) a su app de
{{site.data.keyword.Bluemix_notm}} o a otro [consumidor externo](/docs/resources?topic=resources-externalapp) para que se conecte al servicio.

Para añadir manualmente las credenciales a las apps, consulte la documentación para el tipo de app u opción de cálculo que esté utilizando.
{: tip}

## Adición de una credencial al enlazar un servicio habilitado para IAM
{: #IAM}

Los servicios gestionados por {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) pueden generar una clave de recurso, también conocida como credencial. Las credenciales son específicas del servicio y varían en función de cómo define cada servicio las credenciales que necesita generar. Una credencial puede contener un nombre de usuario, una contraseña, un nombre de host, un puerto y una URL.

Sin embargo, el contenido de cada credencial es exclusivo para el servicio que la genera, todos los servicios gestionados por IAM requieren esas nuevas credenciales incluidas en un rol de acceso al servicio de IAM. Algunos servicios pueden generar más datos que requieren que se pasen parámetros. Por ejemplo, un servicio puede necesitar que especifique un parámetro de idioma para establecer el idioma predeterminado devuelto en la clave de recurso que se genera.

Complete los siguientes pasos para añadir una credencial a un servicio gestionado por IAM:

1. En la lista de recursos, seleccione el nombre del servicio para abrir la página de detalles del servicio. A continuación, seleccione el separador Credenciales y pulse **Credencial nueva +**.
2. En el diálogo Añadir credencial nueva, proporcione un **Nombre**.
3. Especifique el rol. Este valor define el rol de acceso al servicio de IAM. Para obtener más información, consulte: [Acceso de IAM](/docs/iam?topic=iam-userroles)
4. Opcionalmente, puede proporcionar un ID de servicio permitiendo a IAM generar un valor exclusivo para usted o proporcionando un ID de servicio existente. Para obtener más información, consulte [Cómo crear y trabajar con ID de servicio](/docs/iam?topic=iam-serviceids).
5. Opcionalmente, puede proporcionar más parámetros como objeto JSON válido que contiene parámetros de configuración específicos del servicio, proporcionados en línea o en un archivo.

  La mayoría de los servicios no requieren parámetros adicionales, y para los servicios que sí los requieren, cada servicio define su propia lista exclusiva de parámetros. Para obtener una lista de parámetros de configuración soportados, consulte la documentación para ver la oferta de servicios concreta.
  {: note}
6. Pulse **Añadir** para generar la nueva credencial de servicio.

## Adición de una credencial al enlazar un servicio de Cloud Foundry
{: #cf_credential}

Los servicios de Cloud Foundry pueden generar una clave de servicio, también conocida como credencial. Las credenciales son específicas del servicio y varían en función de cómo define cada servicio las credenciales que necesita generar. Una credencial de servicio puede contener un nombre de usuario, una contraseña, un nombre de host, un puerto y una URL.

Sin embargo, el contenido de cada credencial es exclusivo para el servicio que la genera. Algunos servicios pueden generar datos adicionales que requieren que se pasen parámetros. Por ejemplo, un servicio puede necesitar que especifique un parámetro de idioma para establecer el idioma predeterminado devuelto en la clave de servicio que se genera.

Siga estos pasos para añadir una credencial de Cloud Foundry:

1. En la página de detalles de servicio, seleccione el separador Credenciales y pulse **Credencial nueva +**.
2. En el diálogo Añadir credencial nueva, proporcione un **Nombre**.
3. Opcionalmente, puede proporcionar más parámetros como objeto JSON válido que contiene parámetros de configuración específicos del servicio, proporcionados en línea o en un archivo.

  La mayoría de los servicios no requieren parámetros adicionales, y para los servicios que sí los requieren, cada servicio define su propia lista exclusiva de parámetros. Para obtener una lista de parámetros de configuración soportados, consulte la documentación para ver la oferta de servicios concreta.
  {: note}
4. Pulse **Añadir** para generar la nueva credencial de servicio.

## Visualización de una credencial
{: #viewing-credentials}

Después de que se cree una credencial para un servicio, la pueden ver en cualquier momento los usuarios que necesiten el valor de la clave de API. Sin embargo, todos los usuarios deben tener el nivel correcto de acceso para poder ver los detalles de una credencial, incluido el valor de la clave de API. El acceso del usuario debe ser igual o superior al de la credencial de servicio. Por ejemplo, si la credencial tiene el rol de servicio de IAM de `Escritor`, el usuario que desee ver la credencial debe tener asignado el rol de servicio de IAM de `Escritor` o de `Gestor` para dicho servicio. Si un usuario no tiene el acceso correcto, se censuran detalles, como el valor de la clave de API.

Para ver una credencial de servicio existente para un servicio, siga estos pasos:

1. En la lista de recursos, seleccione el nombre del servicio para abrir la página de detalles del servicio. 
2. Pulse **Credenciales de servicio**
3. Amplíe **Ver credenciales** en la fila de una credencial existente.


