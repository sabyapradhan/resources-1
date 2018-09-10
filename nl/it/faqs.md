---

copyright:

  years: 2015, 2018
  
lastupdated: "2018-08-29"

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Domande frequenti
{: #resources-faq}

## Che cosa è un gruppo di risorse?
{: #resource-group}

Un gruppo di risorse è un modo per organizzare le risorse dell'account in raggruppamenti personalizzabili. Qualsiasi risorsa dell'account gestita attraverso il controllo dell'accesso {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartiene a un gruppo di risorse all'interno del tuo account. Assegni le risorse a un gruppo di risorse quando le crei dal catalogo. Puoi quindi visualizzare l'utilizzo del gruppo di risorse nel tuo account e assegnare facilmente agli utenti l'accesso a tutte le risorse in un gruppo di risorse o a una sola risorsa nel gruppo.

Per ulteriori informazioni sulla creazione e sull'utilizzo dei gruppi di risorse, vedi [Gestione dei gruppi di risorse](/docs/resources/resourcegroups.html#rgs).  

## Perché devo migrare le mie istanze del servizio Cloud Foundry a un gruppo di risorse?
{: #instance-migrated}

La migrazione dei servizi Cloud Foundry a un gruppo di risorse indica che i servizi che stai utilizzando sono ora disponibili per l'utilizzo con i gruppi di risorse e il controllo dell'accesso IAM. Puoi trarre vantaggio dal controllo dell'accesso dettagliato utilizzando i ruoli IAM. Puoi inoltre visualizzare l'utilizzo del gruppo di risorse nel tuo account. 

Quando disponi di servizi Cloud Foundry che possono essere migrati a un gruppo di risorse, ricevi una notifica nel tuo dashboard. Per ulteriori informazioni sul processo di migrazione, consulta [Migrazione di applicazioni e istanze del servizio Cloud Foundry a un gruppo di risorse](/docs/resources/instance_migration.html#migrate).

## Perché non posso creare una risorsa e aggiungerla a un gruppo di risorse?
{: #create-add-resource}

Molto probabilmente stai riscontrando un problema di accesso. Devi avere almeno il ruolo di visualizzatore per il gruppo di risorse stesso e almeno il ruolo di editor per il servizio nell'account. Puoi contattare l'amministratore dell'account per verificare il tuo accesso assegnato nell'account. 

## Chi può creare i gruppi di risorse?
{: #create-resource}

Puoi creare i gruppi di risorse solo se ti è stato assegnato il ruolo di amministratore in tutti i servizi abilitati IAM {{site.data.keyword.Bluemix_notm}} nell'account.

## Posso eliminare un gruppo di risorse?
{: #delete-resource-group}

Non puoi eliminare un gruppo di risorse dopo averlo creato.

## Posso spostare le istanze del servizio tra i gruppi di risorse?
{: #instances-between-rgs}

Non puoi spostare le istanze del servizio tra i gruppi di risorse. Se assegni un'istanza del servizio in modo non corretto, devi eliminare e creare nuovamente l'istanza per assegnarla al gruppo di risorse corretto.  

## Posso visualizzare l'utilizzo del gruppo di risorse?
{: #view-usage}

Sì, puoi. Per aprire la pagina Usage Dashboard, fai clic su **Manage > Billing and Usage > Usage**. Puoi visualizzare un riepilogo dell'utilizzo per gruppo di risorse per l'account.  
