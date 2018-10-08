---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolución de problemas de servicios y recursos
{: #services}

Los problemas de los servicios de {{site.data.keyword.Bluemix}} pueden incluir cuestiones relacionadas con la supresión de instancias de servicio. Puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## ¿Por qué no puedo suprimir mi instancia de servicio?
{: #ts_service_broker}

Es posible que reciba un mensaje de error si intenta suprimir una instancia de servicio que ya se ha suprimido desde el controlador de la nube.
{:shortdesc}

Cuando intenta suprimir una instancia de servicio, aparece el siguiente mensaje de error:
{: tsSymptoms}

`Tiempo de espera excedido de pasarela`

Este problema sucede si la instancia de servicio ya se ha suprimido desde el controlador de la nube.
{: tsCauses}

Cree una instancia de servicio con el mismo nombre de servicio y enlácela con las aplicaciones. A continuación, puede suprimir la instancia de servicio y las aplicaciones que utilizan el servicio.   
{: tsResolve}
