---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Resolución de problemas de servicios y recursos
{: #services}

Los problemas generales con servicios y recursos pueden incluir problemas con la supresión de instancias de servicio o problemas con la migración de servicios. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## ¿Por qué no puedo suprimir mi instancia de servicio?
{: #ts_service_broker}
{: troubleshoot}

Es posible que reciba un mensaje de error si intenta suprimir una instancia de servicio que ya se ha suprimido desde el controlador de la nube.
{:shortdesc}

Cuando intenta suprimir una instancia de servicio, aparece el siguiente mensaje de error:
{: tsSymptoms}

`Tiempo de espera excedido de pasarela`

Este problema sucede si la instancia de servicio ya se ha suprimido desde el controlador de la nube.
{: tsCauses}

Cree una instancia de servicio con el mismo nombre de servicio y enlácela con las aplicaciones. A continuación, puede suprimir la instancia de servicio y las aplicaciones que utilizan el servicio.   
{: tsResolve}

## ¿Por qué se ha migrado una instancia de servicio al grupo de recursos incorrecto? 
{: #ts_service_instance}
{: troubleshoot}

Es posible que observe que una instancia de servicio se ha migrado al grupo de recursos incorrecto y no se puede volver a asignar. 
{:shortdesc}

No puede mover los recursos entre grupos de recursos cuando ya estén asignados.
{: tsSymptoms}

Ha asignado la instancia al grupo de recursos incorrecto.  
{: tsCauses}

Para solucionar este problema, intente suprimir la instancia y crear una nueva desde el catálogo. Puede asignarla al grupo de recursos correcto cuando se crea la nueva instancia.
{: tsResolve}

## ¿Por qué no puedo migrar una instancia apta?
{: #ts_migrate_instance}
{: troubleshoot}

Como usuario de la cuenta, está teniendo problemas al migrar una instancia apta. 
{:shortdesc}

No se puede migrar una instancia apta. 
{: tsSymptoms}

Si no puede migrar una instancia apta, es posible que no tenga el acceso correcto. 
{: tsCauses}

Los usuarios deben tener acceso específico para migrar una instancia. Para comprobar el acceso que tiene, pulse **Gestionar** &gt; **Acceso (IAM)** en la barra de menús de la consola y, a continuación, pulse **Usuarios**. Pulse el nombre y revise las políticas de acceso de los roles IAM asignados y el acceso de Cloud Foundry para ver a qué organizaciones tiene acceso y los roles de Cloud Foundry que tiene asignados. 
{: tsResolve}

## ¿Por qué no puedo migrar todos mis servicios?
{: #ts_service_migration}
{: troubleshoot}

No todos los servicios son aptos para la migración. 
{:shortdesc}

No puede migrar determinados servicios. 
{: tsSymptoms}

Está intentando migrar servicios que no están disponibles para que se añadan a grupos de recursos y que no se gestionan mediante Identity and Access Management (IAM). Si un servicio no es apto, no hay ninguna opción para la migración. 
{: tsCauses}

Compruebe los servicios para confirmar que son aptos para la migración. Recibirá una notificación y verá un distintivo `support_rc_migration` que indica si un servicio es apto para la migración.
{: tsResolve}
