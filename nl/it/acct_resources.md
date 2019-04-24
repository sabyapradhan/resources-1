---

copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}


# Che cosa è una risorsa?
{: #resource}

Una risorsa è qualsiasi cosa possa essere creata, gestita e contenuta in un [gruppo di risorse](/docs/resources?topic=resources-rgs). Alcuni esempi includono le applicazioni, le istanze del servizio, i cluster del contenitore, i volumi di archiviazione e i server virtuali. Tutte le istanze del servizio che possono essere aggiunte a un gruppo di risorse quando vengono create dal catalogo sono denominate risorse e sono gestite utilizzando il controllo dell'accesso IAM. I servizi che supportano l'utilizzo dei [ruoli IAM per l'accesso](/docs/iam?topic=iam-userroles#iamusermanrol) e l'organizzazione all'interno del gruppo di risorse sono servizi abilitati IAM.

Attualmente non tutti i servizi supportano l'utilizzo di gruppi di risorse e IAM. Tutte le istanze del servizio che vengono aggiunte alle organizzazioni e agli spazi Cloud Foundry quando sono create dal catalogo sono nettamente diverse dai servizi abilitati a IAM. I servizi Cloud Foundry non hanno connessioni ai gruppi di risorse e utilizzano i [ruoli Cloud Foundry per la gestione dell'accesso](/docs/iam?topic=iam-cfaccess#cfroles). Questi servizi vengono chiamati servizi Cloud Foundry. Poiché i servizi abilitano il supporto per IAM e i gruppi di risorse, ti viene inviata una notifica sulla capacità di [migrare le istanze Cloud Foundry esistenti a un gruppo di risorse](/docs/resources?topic=resources-migrate).


