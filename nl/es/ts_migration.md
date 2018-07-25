---

copyright:

  years: 2018

lastupdated: "2018-07-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Resolución de problemas de migración de instancias de servicio

Si se encuentra con problemas cuando migre una instancia de servicio de Cloud Foundry a un grupo de recursos, revise los problemas comunes siguientes para ayudarle a avanzar.

## Una instancia de servicio se ha migrado al grupo de recursos incorrecto

No puede mover los recursos entre grupos de recursos cuando ya estén asignados. Por lo tanto, si ha asignado una instancia al grupo de recursos incorrecto, intente suprimir la instancia y crear una nueva desde el catálogo. Puede asignarla al grupo de recursos correcto cuando se crea la instancia.

## Un usuario de la cuenta no puede migrar una instancia elegible

Es posible que no se le asigne el acceso correcto para migrar una instancia de servicio. Para obtener más información, consulte [Quién puede migrar instancias de servicio](/docs/resources/instance_migration.html#whocanmigrate).

## Todos los servicios no son elegibles para la migración

No todos los servicios están disponibles para añadirse a grupos de recursos ni a utilizar Identity and Access Management. Cuando los servicios sean elegibles, se le notificará si dispone del acceso para completar la tarea de migración.
