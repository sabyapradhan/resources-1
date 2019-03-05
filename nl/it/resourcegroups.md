---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:note: .note}

# Gestione dei gruppi di risorse
{: #rgs}

Un gruppo di risorse è un modo per organizzare le risorse dell'account in raggruppamenti personalizzabili, in modo da poter assegnare rapidamente agli utenti l'accesso a più di una risorsa alla volta. Qualsiasi risorsa dell'account gestita attraverso il controllo dell'accesso {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartiene a un gruppo di risorse all'interno del tuo account. I servizi Cloud Foundry sono assegnati alle organizzazioni e agli spazi e non possono essere aggiunti a un gruppo di risorse.

Per iniziare a gestire i tuoi gruppi di risorse, vai a **Gestisci** &gt; **Account**. Espandi **Risorse account** e seleziona quindi **Gruppi di risorse**. Da lì puoi visualizzare i tuoi gruppi di risorse, aggiungere risorse, rinominarle, gestire l'accesso e creare nuovi gruppi di risorse. Per ulteriori informazioni sull'utilizzo dei gruppi di risorse, consulta [Procedure consigliate per l'organizzazione delle risorse nei gruppi di risorse](/docs/resources?topic=resources-bp_resourcegroups).


## Creazione di un gruppo di risorse
{: #create_rgs}

Se disponi di un account Pagamento a consumo o Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Puoi anche raggruppare le risorse per facilitare l'assegnazione dell'accesso degli utenti a più di un'istanza alla volta. È importante notare che puoi rinominare un gruppo di risorse ma non puoi eliminarlo dopo che è stato creato.

Se disponi di un account Lite o una prova gratuita di 30 giorni, non puoi creare ulteriori gruppi di risorse, ma puoi rinominare il tuo gruppo di risorse predefinito.

Le connessioni tra un gruppo di risorse e un'organizzazione o uno spazio Cloud Foundry sono limitate dalla tua quota. Per ulteriori informazioni, vedi [Cos'è un alias?](/docs/resources?topic=resources-connect_app#what_is_alias).
{: note}

1. Vai a **Gestisci** &gt; **Account**. Espandi **Risorse account** e seleziona quindi **Gruppi di risorse**. 
2. Fai clic su **Crea un gruppo di risorse**.
3. Immetti un nome per il tuo gruppo di risorse.
4. Fai clic su **Aggiungi**.

## Aggiunta di risorse a un gruppo di risorse
{: #add_to_rgs}

I servizi che sono gestiti con IAM appartengono a un gruppo di risorse invece che a un'organizzazione o uno spazio Cloud Foundry. Quando crei un'istanza del servizio per uno di questi servizi dal catalogo, ti viene richiesto di assegnare l'istanza ad un gruppo di risorse. La tua selezione del gruppo di risorse al momento della creazione dell'istanza è finale e non può essere modificata.

Perché gli utenti nel tuo account possano creare risorse dal catalogo e assegnarle a un gruppo di risorse, è necessario che ad essi siano assegnate due politiche di accesso:

* Una politica con il ruolo di visualizzatore o superiore sul gruppo di risorse stesso
* Una politica con il ruolo di editor o superiore sul servizio nell'account

## Visualizzazione delle risorse nei gruppi di risorse
{: #view_rg_resources}

Per visualizzare facilmente le risorse contenute in un gruppo di risorse, filtra in base al gruppo di risorse dal tuo elenco risorse.

## Ridenominazione di un gruppo di risorse
{: #rename_rgs}

Il tuo primo gruppo di risorse viene creato e denominato `Default` automaticamente. Puoi scegliere di aggiornare il nome di questo gruppo o di qualsiasi altro gruppo che hai creato.

1. Vai a **Gestisci** &gt; **Account**. Espandi **Risorse account** e seleziona quindi **Gruppi di risorse**. 
2. Seleziona **Rinomina** dal menu **Azioni** ![Icona di elenco di azioni](../icons/action-menu-icon.svg).
3. Immetti un nome univoco e fai clic su **Salva**.

## Gestione dei gruppi di risorse e delle risorse utilizzando la CLI {{site.data.keyword.Bluemix_notm}}
{: #rgs_cli}

La CLI {{site.data.keyword.Bluemix_notm}} ha diversi comandi che supportano la gestione delle risorse. Per ulteriori informazioni, vedi [Gestione di risorse e gruppi di risorse](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource#ibmcloud_commands_resource).

## Gestione dell'accesso ai tuoi gruppi di risorse
{: #rgs_manage_access}

Cloud IAM ti offre la possibilità di fornire all'utente l'accesso dettagliato alle risorse nel tuo account. Puoi utilizzare Cloud IAM per assegnare politiche agli utenti, che forniscono all'utente l'accesso a tutte le risorse in un gruppo di risorse, a un singolo tipo di servizio all'interno di un gruppo di risorse o a una singola istanza del servizio nell'account. Fornire agli utenti l'accesso alle risorse all'interno di un gruppo di risorse non dà loro l'accesso per gestire il gruppo di risorse stesso. Puoi impostare l'accesso per la possibilità di visualizzare, modificare e gestire separatamente il gruppo di risorse effettivo.

Per ulteriori informazioni, vedi [Gestione dell'accesso alle risorse](/docs/iam?topic=iam-iammanidaccser).
