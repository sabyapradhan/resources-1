---

copyright:

  years: 2018
lastupdated: "2018-11-15"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Procedure ottimali per organizzare le risorse in un gruppo di risorse
{: #bp_resourcegroups}

Un gruppo di risorse è una funzione che usi per organizzare le [risorse](/docs/resources/acct_resources.html#resource) del tuo account per scopi di controllo dell'accesso e fatturazione. Se hai dimestichezza con l'utilizzo di spazio Cloud Foundry, pensa all'organizzazione delle risorse in gruppi di risorse come qualcosa di simile al modo in cui organizzavi le risorse negli spazi. Una risorsa è qualsiasi cosa possa essere creata, gestita e contenuta in un gruppo di risorse. Gli utenti non vengono aggiunti ai gruppi di risorse. Solo le risorse possono essere aggiunte. 

Al momento, non tutti i servizi supportano l'utilizzo del controllo dell'accesso {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management) e l'assegnazione a un gruppo di risorse. I servizi abilitati a IAM ti richiedono di assegnare le nuove istanze del servizio a un gruppo di risorse quando ne esegui la creazione dal catalogo. L'accesso alle risorse in un gruppo di risorse e al gruppo stesso viene gestito da IAM. Utilizzando i ruoli IAM, puoi fornire agli utenti l'accesso alle risorse organizzate all'interno dei gruppi di risorse. I ruoli IAM possono inoltre fornire la capacità di visualizzare, modificare, aggiungere nuove istanze o gestire l'accesso a un gruppo di risorse.

Puoi anche trovare un elenco di servizi abilitati a IAM quando assegni l'accesso alle risorse dalla IU Identità e accesso completando la seguente procedura:
1. Vai a **Gestisci** &gt; **Accesso (IAM)** e seleziona **Utenti**. 
2. Seleziona un qualsiasi utente e fai clic su **Politiche di accesso**. 
3. Seleziona **Assegna accesso** > **Assegna l'accesso alle risorse**.
4. Utilizzando il menu **Servizi**, seleziona il servizio che vuoi assegnare. Per tutti i servizi che ancora non supportano l'utilizzo di IAM, puoi continuare ad utilizzare i ruoli, gli spazi e le organizzazioni Cloud Foundry. 
5. Fai clic su **Assegna**.

I ruoli, gli spazi e le organizzazioni Cloud Foundry sono chiaramente separati dai gruppi di risorse e dai ruoli IAM. Un ruolo Cloud Foundry non può mai concedere l'accesso alle risorse all'interno di un gruppo di risorse.
{: note}


## Configurazione dei tuoi gruppi di risorse

Tutti gli utenti ottengono un solo gruppo di risorse per impostazione predefinita che può essere ridenominato. Se hai un account fatturabile, puoi creare più di un gruppo di risorse per organizzare le tue risorse. Organizzando le risorse in gruppi di risorse differenti, puoi:

* Assegnare l'accesso a una serie di risorse più facilmente utilizzando un numero minimo di politiche 
* Visualizzare le informazioni di utilizzo per il gruppo di risorse per scopi di fatturazione 

Per creare un nuovo gruppo di risorse, effettua le seguenti operazioni:

1. Vai a **Gestisci** > **Account**.  
2. Espandi **Risorse account** e seleziona **Gruppi di risorse**. 
3. Fai clic su **Crea un gruppo di risorse**.
4. Immetti un nome per il tuo gruppo di risorse.
5. Fai clic su **Aggiungi**.


## Aggiunta di risorse a un gruppo di risorse

I servizi abilitati utilizzando il controllo dell'accesso IAM appartengono a un gruppo di risorse invece che a un'organizzazione o uno spazio Cloud Foundry. Quando crei un'istanza del servizio per uno di questi servizi dal catalogo, ti viene richiesto di assegnare l'istanza ad un gruppo di risorse.  

**Importante**: la tua selezione del gruppo di risorse al momento della creazione dell'istanza è finale e non può essere modificata.

Col crescere del numero di servizi che abilitano l'assegnazione ai gruppi di risorse e l'utilizzo del controllo dell'accesso IAM, ti viene inviata una notifica sul tuo elenco risorse se hai istanze del servizio Cloud Foundry idonee per la migrazione. [Migrando un'istanza del servizio a un gruppo di risorse](/docs/resources/instance_migration.html), stai creando una nuova istanza collegata a un gruppo di risorse di tua scelta e l'istanza Cloud Foundry diventa un alias. 


## Assegnazione dell'accesso ai gruppi di risorse e alle risorse al loro interno

Fornisci l'accesso per gli utenti o i gruppi di utenti organizzati in gruppi di accesso creando le politiche di accesso. Le politiche di accesso impostano una destinazione, normalmente un'istanza del servizio o tutte le istanze di un servizio in un gruppo di risorse e un ruolo, che definisce quale tipo di accesso viene consentito. Esistono due tipi di politiche di accesso di cui hai bisogno da assegnare a un proprietario dell'account per abilitare gli utenti ad accedere al tuo account per utilizzare le risorse nei gruppi di risorse:

* Accesso alle risorse all'interno di un gruppo di risorse. L'accesso può essere concesso a tutte le risorse in un gruppo o soltanto a servizi selezionati in un gruppo.
* Accesso per abilitare gli utenti a gestire il gruppo, il che significa che gli utenti possono visualizzare il gruppo, modificarne il nome, gestire l'accesso perché altri gestiscano il gruppo e soprattutto creare e aggiungere nuove istanze del servizio a un gruppo.

Controlla la seguente tabella per ulteriori informazioni sui due tipi di accesso e cosa consente di fare a un utente ogni ruolo IAM della piattaforma assegnato:

| Dettagli della politica di accesso  | Azioni per l'accesso ai gruppi di risorse | Azione sulle risorse nei gruppi di risorse | 
|:-----------------|:--------------|:---------------|
| Assegna accesso a | Gruppo di risorse selezionato | Servizio selezionato in un gruppo di risorse |
| Ruolo visualizzatore  | Visualizzare il gruppo e le sue caratteristiche ma non le risorse nel gruppo. | Visualizzare le risorse nel gruppo. | 
| Ruolo operatore | Non applicabile | Non applicabile | 
| Ruolo editor | Visualizzare o modificare il nome o altre caratteristiche del gruppo ma non le risorse nel gruppo. | Creare, eliminare, modificare, sospendere, riprendere, visualizzare, associare e gestire l'accesso alle risorse nel gruppo di risorse. |
| Ruolo amministratore |  Visualizzare, modificare o gestire l'accesso al gruppo ma non alle risorse nel gruppo | Creare, eliminare, modificare, sospendere, riprendere, visualizzare, associare e gestire l'accesso alle risorse nel gruppo di risorse. | 
{: caption="Tabella 1. Accesso ai gruppi di risorse" caption-side="top"}

Se vuoi che un utente crei una nuova istanza del servizio e la aggiunga a un gruppo di risorse, l'utente deve essere assegnato come Visualizzatore o ruolo superiore sul gruppo di risorse e Editor o ruolo superiore sul servizio.
{: tip}


## Politiche di accesso di esempio

Controlla le seguenti politiche di accesso di esempio per aiutarti a determinare come potresti assegnare l'accesso alle risorse nel tuo account che appartengono ai gruppi di risorse.

1. Una politica che concede all'utente il ruolo della piattaforma “Amministratore” in {{site.data.keyword.Bluemix_notm}} Container Service nell'intero account. Una politica con questi dettagli consente all'utente di accedere a tutte le istanze di questo servizio e di creare le istanze del servizio in qualsiasi gruppo di risorse in cui l'utente ha un ruolo di visualizzatore. Gli utenti con il ruolo di amministratore in una qualsiasi risorsa possono concedere anche ad altri utenti l'accesso a tale risorsa.
2. Una politica che concede all'utente il ruolo della piattaforma “Visualizzatore” in un gruppo di risorse, ma non alle sue risorse membro. Una politica con questi dettagli consente all'utente la visibilità del gruppo di risorse, che è obbligatoria per creare le istanze di ogni servizio in questo gruppo di risorse.
3. Una politica che concede all'utente il ruolo della piattaforma “Editor” per tutte le risorse nel gruppo di risorse. Un utente con il ruolo di editor in una risorsa può modificare o eliminare tale risorsa.
4. Una politica che concede all'utente il ruolo della piattaforma “Amministratore” nell'intero account (tutti i servizi gestiti IAM). Una politica con questi dettagli consente all'utente di eseguire tutte le azioni della piattaforma su qualsiasi risorsa nell'intero account e inoltre include la capacità di eseguire le azioni di gestione della piattaforma nell'account come la gestione dei gruppi di risorse nell'account.

## Esempi di casi di utilizzo

Per ognuno di questi casi di utilizzo, se hai un gruppo di utenti che vuoi abbiano tutti lo stesso livello di accesso, aggiungili a un [gruppo di accesso](/docs/iam/groups.html#groups). Utilizzando i gruppi di accesso, puoi usare un numero minimo di politiche di accesso poiché tutti i membri del gruppo di accesso ereditano qualsiasi accesso assegnato al gruppo.
{: tip}

<ol>
<li><p>Ho un piccolo account con solo 10 utenti che lavorano insieme su un solo progetto. Alcuni di questi utenti devono gestire l'account e assegnare ad altri utenti l'accesso. Alcuni degli utenti devono eseguire il provisioning delle istanze del servizio, cosa che comporterà delle spese. Altri utenti sono sviluppatori dell'applicazione che devono solo utilizzare le istanze del servizio dai loro componenti dell'applicazione.</p>
<p>A tutti questi utenti dovrebbero essere concessi vari ruoli sull'account e sul gruppo di risorse predefinito - non c'è bisogno di creare ulteriori gruppi di risorse per separare le risorse o limitare alcuni utenti dall'accedere ad alcune risorse. Agli utenti possono essere concessi i ruoli sull'account e sul gruppo di risorse predefinito appropriati alle loro esigenze - amministratore sull'account per gli utenti che devono gestire l'account e fornire ad altri l'accesso, editor sul gruppo di risorse predefinito e i suoi membri per gli utenti che devono eseguire il provisioning delle istanze del servizio e scrittore o lettore sui membri del gruppo di risorse per gli utenti che hanno soltanto bisogno di utilizzare le istanze del servizio.</p>
</li>
<li><p>Ho un account che include tre diversi team che lavorano su tre progetti. Alcuni utenti sono amministratori e hanno bisogno di poter creare nuovi gruppi di risorse e assegnare agli utenti l'accesso ai gruppi di risorse. Gli utenti rimanenti hanno bisogno di accedere soltanto al gruppo di risorse associato ai propri progetti.</p>
<p>Vorrei assegnare agli amministratori il ruolo di amministratore su tutti i servizi abilitati a IAM. Vorrei assegnare agli utenti rimanenti vari ruoli sul gruppo di risorse e sui membri del gruppo di risorse associati al loro progetto – editor del gruppo di risorse per quelli che devono creare le istanze, più scrittore o lettore del membro del gruppo di risorse per quelli che devono utilizzare le istanze.</p>
</li>
<li><p>Ho un account con più gruppi di risorse. Ho alcuni utenti che sono amministratori del servizio A in tutto il mio account e hanno bisogno di accedere a tutte le istanze di tale servizio nonché della capacità di creare le istanze, ma questi utenti non hanno bisogno di accedere a tutte le altre risorse nell'account.</p>
<p>Vorrei assegnare a tre utenti il ruolo di amministratore per il servizio A al livello dell'account, nonché assegnare loro il ruolo di visualizzatore per tutti i gruppi di risorse nell'account di cui devono creare le istanze.</p>
</li>
<li><p>Ho un utente nel mio account che deve solo accedere a una risorsa specifica in un servizio, ad esempio la capacità di scrivere in un bucket A in IBM Cloud Object Storage. Questo utente non dovrebbe visualizzare i gruppi di risorse nel mio account o accedere ad alcun altro servizio o bucket in questa istanza di Cloud Object Storage.</p> 
<p>Vorrei fornire a questo utente il ruolo di scrittore nel bucket A nell'istanza specifica di Cloud Object Storage. Puoi concedere questa politica utilizzando le interfacce specifiche del servizio (la IU Cloud Object Storage, in questo esempio) oppure la IU di assegnazione dell'accesso principale. La IU specifica per il servizio è consigliata perché ti consente di scegliere da un elenco di risorse, mentre la IU di assegnazione dell'accesso non visualizza le risorse al di sotto del livello dell'istanza del servizio e dovrai immettere manualmente il CRN per assegnare la politica a queste risorse.</p>
</li>
<li><p>Sto attualmente utilizzando le organizzazioni e gli spazi Cloud Foundry ma inizierò utilizzando i gruppi di risorse e i gruppi di accesso per i miei servizi abilitati a IAM. Attualmente, i miei utenti e le mie risorse sono organizzati in organizzazioni per linee di business e gli spazi sono utilizzati per i diversi progetti in una linea di business.</p>
<p>Vorrei utilizzare i gruppi di risorse per organizzare le risorse proprio come facevo con gli spazi, pensando a ciascun gruppo di risorse come a uno spazio di progetto. Vorrei quindi configurare dei gruppi di accesso separati per concedere l'accesso necessario ai miei utenti per i corretti gruppi di risorse a livello del progetto. L'accesso può essere concesso a tutte le risorse in un gruppo di risorse oppure anche solo a un gruppo selezionato di risorse all'interno di un gruppo di risorse. Puoi quindi configurare ciascun gruppo di accesso con differenti livelli di accesso alle risorse in un gruppo di risorse, concedendo a ciascun gruppo di utenti l'accesso di cui hanno bisogno per lavorare con le risorse o il gruppo di risorse stesso.</p>
</li>
</ol>


