---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-16"

---

{:shortdesc: .shortdesc}

# Gestione delle connessioni
{: #connect_app}

Puoi connettere un servizio a un'applicazione {{site.data.keyword.Bluemix}} nuova o esistente dalla scheda **Connessioni** del tuo dashboard del servizio. La connessione di un servizio a un'applicazione crea un bind tra di loro e tu puoi annullare il bind, aggiungere altre connessioni o eliminarle utilizzando la scheda **Connessioni**.

Tuttavia, quando connetti un'istanza del servizio gestito da {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management) a un'applicazione, un alias del servizio gestito da IAM viene creato automaticamente nello spazio corrispondente con le informazioni di bind che hai specificato. Questo alias è rappresentato come un'istanza di servizio del tuo servizio gestito da IAM.
{:shortdesc}

## Cos'è un alias?
{: #what_is_alias}

Un alias è una connessione tra il tuo servizio gestito da IAM all'interno di un gruppo di risorse e un'applicazione all'interno di un'organizzazione o di uno spazio. Nella console {{site.data.keyword.Bluemix_notm}}, la connessione (alias) è rappresentata come un'istanza del servizio. Puoi gestire il tuo alias modificando l'istanza del servizio che rappresenta la connessione.

Gli alias sono come collegamenti simbolici che contengono riferimenti a risorse remote e consentono l'interoperabilità e il riutilizzo di un'istanza in tutta la piattaforma. Ad esempio, puoi creare un'istanza di un servizio in un gruppo di risorse e quindi riutilizzarla da qualsiasi regione disponibile creando un alias in un'organizzazione o uno spazio in quella regione.

Per gli alias si applicano le seguenti regole:

* Non è previsto alcun costo aggiuntivo per un alias, ma ogni alias viene conteggiato nella quota della tua organizzazione.
* Puoi creare un solo alias per ogni spazio nella console {{site.data.keyword.Bluemix_notm}}. Tuttavia, è possibile creare più di un alias per spazio utilizzando la CLI {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Comandi per gestire i gruppi di risorse e le risorse](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).
* Se disponi dell'autorizzazione, puoi creare più connessioni tra il tuo servizio gestito da IAM e un'applicazione in qualsiasi spazio, organizzazione e regione nello stesso account.
* Più connessioni eseguite nello stesso spazio a diverse applicazioni da un'istanza del servizio gestito da IAM utilizzano lo stesso alias.
* L'annullamento del bind di un'istanza del servizio gestito da IAM *non* elimina l'istanza del servizio che rappresenta l'alias.
* L'eliminazione dell'applicazione a cui è connessa la tua istanza del servizio gestito da IAM *non* elimina l'istanza che rappresenta l'alias.
* L'eliminazione di un'istanza del servizio gestito da IAM *elimina* l'istanza del servizio che rappresenta l'alias.

## Creazione di una connessione (alias) tra un servizio gestito da IAM e un'applicazione
{: #creating_alias}

Per connettere la tua istanza del servizio gestito da IAM a un'applicazione:

1. Vai al tuo dashboard.

2. Fai clic sul nome della tua applicazione per aprire la vista dei dettagli.

3. Fai clic su **Connetti esistente** e scegli la tua applicazione esistente. In alternativa, fai clic su **Crea connessione** per creare un'applicazione a cui connetterti.

4. Specifica il **Ruolo di accesso per il collegamento**. Questo valore imposta il ruolo di accesso del servizio IAM. Per ulteriori informazioni, vedi [Accesso IAM](/docs/iam/users_roles.html#userroles).

5. Facoltativamente, puoi fornire un **ID del servizio per il collegamento ** consentendo a IAM di generare per te un valore univoco o fornendo un ID di servizio esistente. Per ulteriori informazioni, vedi [Creazione e gestione degli ID servizio](/docs/iam/serviceid.html#serviceids).

6. Fai clic su **Create**.

## Visualizzazione di un alias

Dopo aver creato una connessione tra un servizio gestito da IAM e un'applicazione, l'alias viene visualizzato nella scheda **Connessioni** dell'applicazione connessa. Inoltre, l'alias viene visualizzato come istanza del servizio in esecuzione sul tuo dashboard e contiene una scheda **Connessioni** solo quando lo apri.

1. Vai al tuo dashboard.
2. Dalla tabella **Servizi dell'applicazione**, fai clic sul nome dell'istanza del servizio per aprire la vista dei dettagli. Se contiene solo una scheda **Connessioni**, è un alias.

## Eliminazione di un alias

Il modo più semplice per eliminare l'alias è eliminare l'istanza del servizio gestito da IAM. Tuttavia, puoi mantenere la tua istanza del servizio gestito da IAM ed eliminare direttamente l'alias.

1. Vai al tuo dashboard.
2. Dalla tabella **Servizi dell'applicazione**, fai clic sul nome dell'istanza del servizio per aprire la vista dei dettagli. Se contiene solo una scheda **Connessioni**, è un alias.
3. Elimina l'istanza.

## Creazione di una connessione tra più servizi
{: #cf}

Per ulteriori informazioni, vedi [Utilizzo di servizi in un altro servizio](/docs/apps/reqnsi.html#add_service).
