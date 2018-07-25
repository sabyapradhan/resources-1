---

copyright:

  years: 2018
lastupdated: "2018-07-17"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# ¿Qué es un recurso?
{: #resource}

Un recurso es cualquier cosa que se pueda crear, gestionar y contener dentro de un [grupo de recursos](/docs/resources/resourcegroups.html#rgs). Algunos ejemplos incluyen apps, instancias de servicio, clústeres de contenedores, volúmenes de almacenamiento y servidores virtuales. Todas las instancias de servicio que se pueden añadir a un grupo de recursos cuando se crean desde el catálogo se llaman recursos y se gestionan utilizando el control de accesos de IAM. Los servicios que soportan el uso de [roles de IAM para el acceso](/docs/iam/users_roles.html#iamusermanrol) y la organización dentro de un grupo de recursos son servicios habilitados por IAM.

No todos los servicios dan soporte al uso de grupos de recursos e IAM en este momento. Todas las instancias de servicio que se añaden a organizaciones y espacios de Cloud Foundry cuando se crean desde el catálogo son marcadamente distintas de los servicios habilitados por IAM. Los servicios de Cloud Foundry no tienen conexión a los grupos de recursos y utilizan [roles de Cloud Foundry para la gestión de acceso](/docs/iam/cfaccess.html#cfaccess). Estos servicios se llaman Servicios de Cloud Foundry. A medida que los servicios habiliten el soporte para IAM y grupos de recursos, se le notificará sobre la posibilidad de [migrar instancias existentes de Cloud Foundry a un grupo de recursos](/docs/resources/instance_migration.html#migrate).

