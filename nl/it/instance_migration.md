---

copyright:

  years: 2017, 2018

lastupdated: "2018-06-20"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migrazione di istanze del servizio Cloud Foundry a un gruppo di risorse
{: #migrate}

Per rendere la tua esperienza con {{site.data.keyword.Bluemix}} più semplice e flessibile, {{site.data.keyword.Bluemix}} ha introdotto i [gruppi di risorse](/docs/resources/resourcegroups.html#rgs), che sono concettualmente simili agli spazi Cloud Foundry. Tuttavia, i gruppi di risorse comprendono numerosi vantaggi aggiuntivi, come il controllo dell'accesso più dettagliato utilizzando IBM IAM (Identity and Access Management), la possibilità di connettere le istanze del servizio ad applicazioni e servizi in diverse regioni e un modo semplice per visualizzare l'utilizzo per ogni gruppo.
{:shortdesc}

{{site.data.keyword.Bluemix_notm}} sta iniziando a spostare servizi da Cloud Foundry per beneficiare dei gruppi di risorse. Quando vedi l'icona ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse") accanto a uno dei tuoi servizi nel dashboard, devi avviare un piano di migrazione affinché le tue istanze del servizio passino dall'organizzazione e spazio Cloud Foundry corrente a un gruppo di risorse. Finché un servizio {{site.data.keyword.Bluemix_notm}} non viene spostato dall'utilizzo dei ruoli, spazi e organizzazioni Cloud Foundry all'utilizzo di IAM e dei gruppi di risorse, non puoi migrare le tue istanze del servizio Cloud Foundry esistenti a un gruppo di risorse.

Quando migri le istanze del servizio Cloud Foundry esistenti a un gruppo di risorse, il gruppo di risorse che scegli non può essere modificato dopo il completamento della migrazione. Pertanto, è essenziale pianificare il modo in cui desideri organizzare le risorse nell'account prima di eseguire la migrazione. Pertanto, potresti dover creare uno o più gruppi di risorse, se disponi di un account fatturabile, prima di eseguire la migrazione. 

Puoi provare a organizzare le tue risorse in gruppi di risorse nello stesso modo in cui hai organizzato le risorse negli spazi Cloud Foundry. Per ulteriori informazioni sull'utilizzo dei gruppi di risorse, consulta [Procedure consigliate per l'organizzazione delle risorse nei gruppi di risorse](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).
{: tip}


## Perché migrare le istanze del servizio?

I servizi che supportano il controllo dell'accesso e l'organizzazione Cloud IAM in gruppi di risorse dispongono di diversi vantaggi:

* Utilizzando il controllo dell'accesso dettagliato, puoi impostare l'accesso alle singole istanze del servizio o a un insieme di risorse organizzate in un gruppo di risorse. 
* Utilizzando i gruppi di accesso e di risorse per organizzare gli utenti e le risorse, puoi impostare solo il numero minimo di politiche di accesso. Ad esempio, se hai una serie di sviluppatori che vuoi abbiano tutti accesso alle risorse di un ambiente di sviluppo, puoi organizzare tutti questi utenti in un gruppo di accesso di sviluppatori e poi aggiungere tutte le risorse di cui hanno bisogno dell'accesso a un solo gruppo di risorse. Quindi, puoi impostare una sola politica per il gruppo di accesso per avere accesso a tutte le risorse nel gruppo di risorse.
* Puoi visualizzare l'utilizzo dal gruppo di risorse in modo simile a come potresti visualizzare l'utilizzo dalle organizzazioni Cloud Foundry.
* Puoi collegarti alle applicazioni e servizi in ogni spazio Cloud Foundry, che consente le connessioni di applicazioni e servizi da regioni diverse. Quando esegui la migrazione, la connessione viene eseguita automaticamente trasformando la tua istanza del servizio Cloud Foundry originale in un alias e creando un'istanza collegata in un gruppo di risorse a tua scelta. Il seguente grafico illustra come funziona la connessione utilizzando un alias.

![Associazione di un'istanza del servizio a uno spazio Cloud Foundry per creare un alias](images/alias.svg "Associazione di un'istanza del servizio a uno spazio Cloud Foundry per creare un alias")

## Chi può migrare le istanze del servizio?
{: #whocanmigrate}

Gli utenti devono disporre di un accesso specifico per migrare le istanze del servizio Cloud Foundry a un gruppo di risorse:

* Un utente deve avere il ruolo di sviluppatore sullo spazio Cloud Foundry o il ruolo Cloud Foundry di gestore organizzazione sull'organizzazione a cui appartiene l'istanza.
* Un utente deve avere almeno il ruolo IAM di visualizzatore per gestire il gruppo di risorse a cui sarà migrata l'istanza.
* Un utente deve avere almeno il ruolo IAM di editor sul servizio.

Per ulteriori informazioni sull'assegnazione dell'accesso corretto, vedi [Accesso Cloud Foundry](/docs/iam/cfaccess.html#cfaccess) e [Accesso IAM](/docs/iam/users_roles.html#platformrolestable).

Per controllare di quale accesso disponi, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** dalla barra del menu della console e poi fai clic su **Utenti**. Fai clic sul tuo nome ed esamina le tue **Politiche di accesso** per i ruoli IAM assegnati e **Accesso Cloud Foundry** per visualizzare quali sono le organizzazioni a cui hai accesso e i tuoi ruoli Cloud Foundry assegnati.
{: tip}


## Come funziona la migrazione?

Quando esegui la migrazione di un'istanza del servizio da un'organizzazione e uno spazio Cloud Foundry a un gruppo di risorse, viene creata una nuova istanza del servizio collegata nel gruppo di risorse. L'istanza originale nell'organizzazione o spazio Cloud Foundry diventa un [alias](/docs/resources/connecting_apps.html#what_is_alias). L'alias viene conteggiato nella quota per la tua organizzazione ma ti viene addebitato l'utilizzo dell'istanza del servizio nel gruppo di risorse.

![Migrazione di un'istanza del servizio Cloud Foundry a un gruppo di risorse](images/migration.gif){: gif}

Le istanze del servizio vengono migrate una per volta quando ricevi la notifica nel dashboard dall'icona ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse") associata alla tua istanza del servizio Cloud Foundry.

Prima di iniziare il processo di migrazione, controlla la documentazione del servizio per vedere se devono essere apportate ulteriori modifiche specifiche del servizio. Ad esempio, potresti dover migrare i dati dalle vecchie alle nuove istanze o aggiornare le credenziali utilizzate per la tua applicazione se elimini l'alias Cloud Foundry. Le applicazioni che effettuano una chiamata diretta all'API di un servizio che è stato migrato devono aggiornare la chiamata API in modo che utilizzi una chiave API IAM o un token di accesso.
{: tip}

1. Apri il menu **Ulteriori azioni**.
2. Per iniziare, seleziona **Migra a un gruppo di risorse**.
3. Seleziona un gruppo di risorse.
4. Fai clic su **Migra**; l'istanza viene migrata per tuo conto.
5. Poiché puoi migrare solo un'istanza per volta, puoi continuare a migrare le istanze idonee dopo che hai migrato la prima.

Dopo che hai correttamente migrato un'istanza, la visualizzi nella sezione dei servizi del tuo dashboard. L'alias rimane nella sezione Cloud Foundry del dashboard. Puoi utilizzare l'icona ![Icona di link](images/link.svg "Icona di link che rappresenta un alias") nella sezione Cloud Foundry del dashboard per identificare gli alias.

## Passi successivi
{: #nextsteps}

Dopo aver migrato le tue istanze del servizio Cloud Foundry a un gruppo di risorse, devi assicurarti che gli utenti nel tuo account abbiano il livello di accesso necessario per accedere alle risorse nei gruppi di risorse nell'account. Potresti anche voler fornire l'accesso per gestire il gruppo di risorse in modo che gli utenti possano creare nuove istanze del servizio nei gruppi di risorse dell'account.

Per ulteriori informazioni sull'assegnazione dell'accesso alle risorse nei tuoi gruppi di risorse, consulta [Assegnazione dell'accesso ai gruppi di risorse e alle risorse al loro interno](/docs/resources/bestpractice_rgs.html#assigning-access-to-resource-groups-and-the-resources-within-them).

Inoltre, assicurati di consultare la documentazione del servizio per verificare se è necessario apportare aggiornamenti per le tue applicazioni esistenti al termine della migrazione. 


## Risoluzione dei problemi

Se riscontri eventuali problemi di migrazione delle istanze del servizio Cloud Foundry, consulta [Risoluzione dei problemi relativi alla migrazione delle istanze del servizio](/docs/resources/ts_migration.html).
