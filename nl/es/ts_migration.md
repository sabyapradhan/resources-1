---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Resolución de problemas de migración de instancias de servicio

Si se encuentra con problemas mientras realiza la migración de una instancia de servicio de Cloud Foundry a un grupo de recursos, revise los problemas comunes siguientes para ayudarle a avanzar con la migración.

## ¿Qué ocurre si he migrado mi instancia de servicio al grupo de recursos equivocado?

En este momento, no puede mover los recursos entre grupos de recursos cuando ya estén asignados. Por lo tanto, si ha migrado una instancia al grupo de recursos equivocado, intente suprimir la instancia y crear una nueva desde el catálogo. Puede asignarla al grupo de recursos correcto cuando crea la instancia.

## ¿Por qué no puedo realizar la migración?

Es posible que no disponga del acceso asignado correcto para poder migrar a una instancia de servicio. Consulte [Quién puede migrar instancias de servicio](/docs/account/instance_migration.html#whocanmigrate) para obtener más información.

## ¿Por qué no son elegibles para la migración todos mis servicios?

No todos los servicios están disponibles para ser gestionados utilizando el control de acceso IAM y los grupos de recursos en estos momentos. Cuando los servicios habiliten el uso de IAM, se le notificará si dispone de acceso para completar la tarea de migración.
