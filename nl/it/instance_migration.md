---

copyright:

  years: 2017, 2019

lastupdated: "2019-02-19"

keywords: migrate, migrating to a resource group, migrate Cloud Foundry

subcollection: resources

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migrazione di applicazioni e istanze del servizio Cloud Foundry a un gruppo di risorse
{: #migrate}

Per rendere la tua esperienza con l'utilizzo di {{site.data.keyword.Bluemix}} più semplice e flessibile, abbiamo introdotto i [gruppi di risorse](/docs/resources?topic=resources-rgs), che sono concettualmente simili agli spazi Cloud Foundry. Tuttavia, i gruppi di risorse comprendono numerosi vantaggi aggiuntivi, come il controllo dell'accesso più dettagliato utilizzando IBM IAM (Identity and Access Management), la possibilità di connettere le istanze del servizio ad applicazioni e servizi in diverse regioni e un modo semplice per visualizzare l'utilizzo per ogni gruppo.
{:shortdesc}

Stiamo iniziando a spostare i servizi da Cloud Foundry per trarre vantaggio dai gruppi di risorse, il che significa che quando vedi l'icona ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse") accanto a uno dei tuoi servizi nel tuo elenco risorse, devi avviare un piano di migrazione delle tue applicazioni o istanze del servizio create tramite [{{site.data.keyword.Bluemix_notm}} {{site.data.keyword.dev_console}}](https://cloud.ibm.com/developer/appservice/dashboard) per lo spostamento dall'organizzazione e spazio Cloud Foundry in cui attualmente si trovano a un gruppo di risorse. Finché un servizio {{site.data.keyword.Bluemix_notm}} non viene spostato dall'utilizzo dei ruoli, spazi e organizzazioni Cloud Foundry all'utilizzo di IAM e dei gruppi di risorse, non puoi migrare le tue istanze del servizio Cloud Foundry esistenti a un gruppo di risorse.

Quando migri le istanze del servizio Cloud Foundry o le applicazioni {{site.data.keyword.dev_console}} esistenti a un gruppo di risorse, il gruppo che scegli non può essere modificato dopo il completamento della migrazione. Pertanto, è essenziale pianificare il modo in cui desideri organizzare le risorse nell'account prima di eseguire la migrazione. Questo potrebbe voler dire che devi creare uno o più gruppi di risorse, se hai un account fatturabile, prima della migrazione.

Puoi provare a organizzare le tue risorse in gruppi di risorse nello stesso modo in cui hai organizzato le risorse negli spazi Cloud Foundry. Per ulteriori informazioni sull'utilizzo dei gruppi di risorse, consulta [Procedure consigliate per l'organizzazione delle risorse nei gruppi di risorse](/docs/resources?topic=resources-bp_resourcegroups).
{: tip}


## Perché eseguire la migrazione?
{: #why_migrate}

### Istanze del servizio Cloud Foundry
{: #cf_instances}

I servizi che supportano il controllo dell'accesso e l'organizzazione Cloud IAM in gruppi di risorse dispongono di diversi vantaggi:

* Utilizzando il controllo dell'accesso dettagliato, puoi impostare l'accesso alle singole istanze del servizio o a un insieme di risorse organizzate in un gruppo di risorse.
* Utilizzando i gruppi di accesso e di risorse per organizzare gli utenti e le risorse, puoi impostare solo il numero minimo di politiche di accesso. Ad esempio, se hai una serie di sviluppatori che vuoi abbiano tutti accesso alle risorse di un ambiente di sviluppo, puoi organizzare tutti questi utenti in un gruppo di accesso di sviluppatori e poi aggiungere tutte le risorse di cui hanno bisogno dell'accesso a un solo gruppo di risorse. Quindi, puoi impostare una sola politica per il gruppo di accesso per avere accesso a tutte le risorse nel gruppo di risorse.
* Puoi visualizzare l'utilizzo in base al gruppo di risorse in modo simile a come potresti visualizzare l'utilizzo in base alle organizzazioni Cloud Foundry.
* Puoi collegarti alle applicazioni e servizi in ogni spazio Cloud Foundry, che consente le connessioni di applicazioni e servizi da regioni diverse. Quando esegui la migrazione, la connessione viene eseguita automaticamente quando trasformi la tua istanza del servizio Cloud Foundry originale in un alias e crei un'istanza collegata in un gruppo di risorse a tua scelta. Il seguente grafico mostra come funziona la connessione utilizzando un alias.

![Associazione di un'istanza del servizio a uno spazio Cloud Foundry per creare un alias](images/alias.svg "Associazione di un'istanza del servizio a uno spazio Cloud Foundry per creare un alias")

### {{site.data.keyword.dev_console}}apps

{: #app_services}

In precedenza, le applicazioni {{site.data.keyword.dev_console}} potevano essere associate solo alle istanze del servizio Cloud Foundry. Ora, se migri le tue applicazioni a un gruppo di risorse, puoi associarle alle istanze del servizio che appartengono a un gruppo di risorse e supportano il controllo dell'accesso Cloud IAM.

## Chi può eseguire la migrazione?
{: #whocanmigrate}

### Accesso richiesto per le istanze del servizio
{: #required_access_instances}

Gli utenti devono disporre di un accesso specifico per migrare le istanze del servizio Cloud Foundry a un gruppo di risorse:

* Un utente deve avere il ruolo di sviluppatore sullo spazio Cloud Foundry o il ruolo Cloud Foundry di gestore organizzazione sull'organizzazione a cui appartiene l'istanza.
* Un utente deve avere almeno il ruolo IAM di visualizzatore per gestire il gruppo di risorse a cui sarà migrata l'istanza.
* Un utente deve avere almeno il ruolo IAM di editor sul servizio.

Per ulteriori informazioni sull'assegnazione dell'accesso corretto, vedi [Accesso Cloud Foundry](/docs/iam?topic=iam-cfaccess) e [Accesso IAM](/docs/iam?topic=iam-userroles#platformrolestable1).

Per controllare qual è l'accesso di cui disponi, fai clic su **Gestisci** &gt; **Accesso (IAM)** dalla barra dei menu della console e fai quindi clic su **Utenti**. Fai clic sul tuo nome ed esamina le tue **Politiche di accesso** per i ruoli IAM assegnati e **Accesso Cloud Foundry** per visualizzare quali sono le organizzazioni a cui hai accesso e i tuoi ruoli Cloud Foundry assegnati.
{: tip}

### Accesso richiesto per le applicazioni {{site.data.keyword.dev_console}}
{: #required_access_apps}

Qualsiasi utente che può accedere a un'applicazione {{site.data.keyword.dev_console}} può eseguirne la migrazione. Tuttavia, la migrazione di un'applicazione non ne migra i servizi associati. Le istanze del servizio devono essere migrate separatamente.

## Come funziona la migrazione?
{: #how}

### Migrazione delle istanze del servizio
{: #migrate_instances}

Quando esegui la migrazione di un'istanza del servizio da un'organizzazione e uno spazio Cloud Foundry a un gruppo di risorse, viene creata una nuova istanza del servizio collegata nel gruppo di risorse. L'istanza originale nell'organizzazione o spazio Cloud Foundry diventa un [alias](/docs/resources?topic=resources-connect_app#what_is_alias). L'alias viene conteggiato nella quota per la tua organizzazione ma ti viene addebitato l'utilizzo dell'istanza del servizio nel gruppo di risorse.

![Migrazione di un'istanza del servizio Cloud Foundry a un gruppo di risorse](images/migration.gif){: gif}

Le istanze del servizio vengono migrate una per volta quando ricevi la notifica sull'elenco risorse dall'icona ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse") associata alla tua istanza del servizio Cloud Foundry.

Prima di iniziare il processo di migrazione, controlla la documentazione del tuo servizio per vedere se ci sono delle ulteriori modifiche specifiche per il servizio che potresti dover apportare quando migri la tua istanza del servizio a un gruppo di risorse. Ad esempio, potresti dover migrare i dati dalle vecchie alle nuove istanze o aggiornare le credenziali utilizzate per la tua applicazione se elimini l'alias Cloud Foundry. Le applicazioni che effettuano una chiamata diretta all'API di un servizio che viene migrato devono aggiornare la chiamata API in modo che utilizzi una chiave API IAM o un token di accesso.
{: tip}

1. Apri il menu **Ulteriori azioni**.
2. Per iniziare, seleziona **Migra a un gruppo di risorse**.
3. Seleziona un gruppo di risorse.
4. Fai clic su **Migra**; l'istanza viene migrata per tuo conto.
5. Poiché puoi migrare solo un'istanza per volta, puoi continuare a migrare le istanze idonee dopo che hai migrato la prima.

Dopo che hai correttamente migrato un'istanza, la visualizzi nella sezione dei servizi del tuo elenco risorse. L'alias rimane nella sezione Cloud Foundry dell'elenco risorse. Puoi utilizzare l'icona ![Icona di link](images/link.svg "Icona di link che rappresenta un alias") nella sezione Cloud Foundry dell'elenco risorse per identificare gli alias.

### Migrazione delle applicazioni {{site.data.keyword.dev_console}}
{: #migrate_apps}

Le applicazioni vengono migrate una alla volta facendo clic sull'icona ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse") associata ad ogni voce nella tua vista Elenco applicazioni.

1. Seleziona l'icona **Menu** ![Icona menu](../icons/icon_hamburger.svg) e seleziona il portale degli sviluppatori di interesse come ad esempio Watson, Mobile o Applicazioni Web.
2. Seleziona **Applicazioni**, che visualizza gli elenchi **Applicazioni (Azione richiesta)** e **Applicazioni (migrate)**.
3. Per ogni voce nell'elenco **Applicazioni (Azione richiesta)**, fai clic sull'icona **Migra** ![Migra questa istanza del servizio a un gruppo di risorse](images/migrate.svg "Migra questa istanza del servizio a un gruppo di risorse").
4. Seleziona o crea un nuovo gruppo di risorse.
5. Fai clic su **Migra** e l'applicazione viene migrata.
6. Conferma che l'applicazione sia ora visualizzata nell'elenco **Applicazioni (migrate)**.
7. Poiché puoi migrare solo un'applicazione per volta, puoi continuare a migrare le applicazioni idonee dopo che hai migrato la prima.


## Passi successivi
{: #migrate_next_steps}

Dopo aver migrato le tue istanze del servizio Cloud Foundry a un gruppo di risorse, devi assicurarti che gli utenti nel tuo account abbiano il livello di accesso necessario per accedere alle risorse nei gruppi di risorse nell'account. Potresti anche voler fornire l'accesso per gestire il gruppo di risorse in modo che gli utenti possano creare nuove istanze del servizio nei gruppi di risorse dell'account.

Per ulteriori informazioni sull'assegnazione dell'accesso alle risorse nei tuoi gruppi di risorse, consulta [Assegnazione dell'accesso ai gruppi di risorse e alle risorse al loro interno](/docs/resources?topic=resources-bp_resourcegroups#assigning_access_rgs).

Inoltre, assicurati di consultare la documentazione del servizio per verificare se è necessario apportare aggiornamenti per le tue applicazioni esistenti al termine della migrazione.


## Risoluzione dei problemi
{: #ts_migration}

Se riscontri eventuali problemi di migrazione delle istanze del servizio Cloud Foundry, consulta [Risoluzione dei problemi relativi ai servizi e alle risorse](/docs/resources?topic=resources-services).
