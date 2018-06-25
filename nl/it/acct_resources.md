---

copyright:

  years: 2018
lastupdated: "2018-05-07"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Che cosa è una risorsa? 
{: #resource}

Una risorsa è qualsiasi cosa possa essere creata, gestita e contenuta in un [gruppo di risorse](/docs/resources/resourcegroups.html#rgs). Alcuni esempi includono le applicazioni, le istanze del servizio, i cluster del contenitore, i volumi di archiviazione e i server virtuali. Tutte le istanze del servizio che possono essere aggiunte a un gruppo di risorse quando vengono create dal catalogo, vengono denominate risorse e sono gestite utilizzando il controllo dell'accesso IAM. I servizi che supportano l'utilizzo dei [ruoli IAM per l'accesso](/docs/iam/users_roles.html#iamusermanrol) e l'organizzazione all'interno del gruppo di risorse sono servizi abilitati IAM.

Non tutti i servizi supportano l'utilizzo dei gruppi di risorse e IAM in questo momento. Tutte le istanze del servizio aggiunte a spazi e organizzazioni Cloud Foundry quando vengono create dal catalogo, sono chiaramente differenti dai servizi abilitati IAM. I servizi Cloud Foundry non hanno connessioni ai gruppi di risorse e utilizzano i [ruoli Cloud Foundry per la gestione dell'accesso](/docs/iam/cfaccess.html#cfaccess). Questi servizi vengono chiamati servizi Cloud Foundry. Poiché i servizi abilitano il supporto per IAM e i gruppi di risorse, ti viene inviata una notifica sulla capacità di [migrare le istanze Cloud Foundry esistenti a un gruppo di risorse](/docs/resources/instance_migration.html#migrate).


