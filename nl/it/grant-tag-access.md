---

copyright:

  years: 2018
lastupdated: "2018-11-15"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Concessione agli utenti dell'accesso eseguire operazioni di tag sulle risorse	
{: #access}	
	
In qualità di proprietario dell'account, potresti voler delegare parte della responsabilità delle operazioni di tag sulle risorse. Per farlo, puoi concedere l'accesso ad altri utenti nell'account per aggiungere tag alle risorse o per rimuoverle. Per poter aggiungere tag a una risorsa, agli utenti nell'account deve essere assegnato l'accesso appropriato. L'accesso ai servizi che appartengono a un gruppo di risorse è gestito dalle politiche di accesso {{site.data.keyword.Bluemix}} IAM (Identity and Access Management) e l'accesso ai servizi che appartengono a un'organizzazione e uno spazio Cloud Foundry  gestiti dai ruoli per l'organizzazione e lo spazio Cloud Foundry.
{: shortdesc}

## Autorizzazioni delle operazioni di tag
{: #tagging-permissions}

Le tag sono visibili a qualsiasi utente in un account. Dopo essere stata aggiunta a una risorsa, la tag è visibile a tutti gli utenti che hanno accesso in lettura alla risorsa. Per aggiungere o rimuovere una tag da una risorsa, sono necessarie delle specifiche autorizzazioni o degli specifici ruoli di accesso, a seconda del tipo di risorsa. Controlla la seguente tabella per capire quale ruolo è richiesto per ciascun tipo di risorsa. 


| Tipo di risorsa | Ruolo |
|--------|---------------|
| Abilitata a IAM | Editor o Amministratore sulla risorsa | 
| Cloud Foundry | Ruolo Sviluppatore sullo spazio a cui appartiene la risorsa. | 
| Infrastruttura classica* | Autorizzazione di visualizzazione dei dettagli hardware o autorizzazione di visualizzazione dei dettagli del server virtuale |
| Cloud Object Storage S3 sull'infrastruttura classica | Autorizzazione di gestione dell'archiviazione |
{: caption="Tabella 1. Ruoli richiesti per l'aggiunta e la rimozione di tag" caption-side="top"}

*Le risorse su cui è possibile eseguire operazioni di tag nell'infrastruttura classica sono Virtual Guest, Virtual Dedicated Host, Network Application Delivery Controller, Gateway Member, Subnet, VLAN e VLAN Firewall (Dedicated).


## Concessione dell'accesso per l'esecuzione di operazioni di tag sulle risorse abilitate a IAM
{: #iam-managed}

Le risorse che appartengono a un gruppo di risorse sono gestite dalle politiche di accesso {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management). Completa la seguente procedura per assegnare il ruolo Editor per consentire a un utente di eseguire operazioni di tag su risorse abilitate a IAM:

  1. Dalla console {{site.data.keyword.Bluemix_notm}}, fai clic su **Gestisci > Accesso (IAM)** e seleziona **Utenti**.
  2. Fai clic sul nome dell'utente a cui stai concedendo l'accesso. 
  3. Fai clic su **Politiche di accesso** > **Assegna accesso**.
  4. Seleziona l'opzione **Assegna l'accesso alle risorse**.
  5. Dall'elenco di servizi, seleziona un servizio specifico oppure **Tutti i servizi abilitati per l'accesso e l'identità**.
  6. Dall'elenco di ruoli di accesso della piattaforma, seleziona **Editor**. 
  7. Fai clic su **Assegna**.

## Concessione dell'accesso per l'esecuzione di operazioni di tag su risorse Cloud Foundry
{: #cf}

Le risorse che appartengono a un'organizzazione e a uno spazio Cloud Foundry sono gestite dai ruoli di organizzazione e spazio Cloud Foundry. Completa la seguente procedura per assegnare il ruolo dello spazio Sviluppatore per consentire a un utente di eseguire operazioni di tag su risorse Cloud Foundry:

 1. Fai clic su **Gestisci > Accesso (IAM)** e seleziona **Utenti**.
2. Seleziona il nome per l'utente a cui vuoi fornire l'accesso.
3. Fai clic su **Accesso Cloud Foundry**. 
4. Fai clic su **Assegna organizzazione**.
5. Espandi e seleziona l'`Organizzazione` con l'istanza del servizio per cui vuoi fornire l'accesso all'utente. 
6. Seleziona la regione. 
7. Seleziona il ruolo dello spazio **Sviluppatore**.
8. Fai clic su **Salva ruolo**.

## Concessione dell'accesso per l'esecuzione di operazioni di tag su risorse dell'infrastruttura classica
{: #classic-infra}

Completa la seguente procedura per assegnare il ruolo di accesso ai servizi Gestore per consentire a un utente di eseguire operazioni di tag sui servizi dell'infrastruttura classica.

  1. Fai clic su **Gestisci > Accesso (IAM)** e seleziona **Utenti**.
  2. Fai clic sul nome dell'utente a cui stai concedendo l'accesso.
  3. Fai clic su **Infrastruttura classica**
  4. Dalla scheda **Autorizzazioni**, espandi la categoria **Dispositivi**.
  5. Seleziona **Visualizza dettagli hardware** e **Visualizza dettagli server virtuale**. Se devi assegnare l'accesso a Cloud Object Storage S3, assegna l'autorizzazione **Gestione archiviazione**.
  6. Fai clic su **Salva**.
  7. Fai clic sulla scheda **Dispositivi**.
  8. Seleziona **Tutti i server bare metal** oppure **Tutti i server virtuali**, a seconda della risorsa su cui vuoi eseguire operazioni di tag.

