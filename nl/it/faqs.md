---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-07"

keywords: resource FAQs, resource frequently asked questions

subcollection: resources

---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# Domande frequenti
{: #resources-faq}

## Che cosa è un gruppo di risorse?
{: #resource-group}
{: faq}

Un gruppo di risorse è un modo per organizzare le risorse dell'account in raggruppamenti personalizzabili. Qualsiasi risorsa dell'account gestita attraverso il controllo dell'accesso {{site.data.keyword.Bluemix}} IAM (Identity and Access Management) appartiene a un gruppo di risorse all'interno del tuo account. Assegni le risorse a un gruppo di risorse quando ne esegui la creazione dal catalogo. Puoi quindi visualizzare l'utilizzo del gruppo di risorse nel tuo account e assegnare facilmente agli utenti l'accesso a tutte le risorse in un gruppo di risorse o a una sola risorsa nel gruppo.

Per ulteriori informazioni sulla creazione e sull'utilizzo dei gruppi di risorse, vedi [Gestione dei gruppi di risorse](/docs/resources?topic=resources-rgs).  

## Perché devo migrare le mie istanze del servizio Cloud Foundry a un gruppo di risorse?
{: #instance-migrated}
{: faq}

La migrazione dei servizi Cloud Foundry a un gruppo di risorse indica che i servizi che stai utilizzando sono ora disponibili per l'utilizzo con i gruppi di risorse e il controllo dell'accesso IAM. Puoi trarre vantaggio dal controllo dell'accesso dettagliato utilizzando i ruoli IAM. Puoi inoltre visualizzare l'utilizzo del gruppo di risorse nel tuo account.

Quando disponi di servizi Cloud Foundry che possono essere migrati a un gruppo di risorse, ricevi una notifica sul tuo elenco di risorse. Per ulteriori informazioni sul processo di migrazione, consulta [Migrazione di applicazioni e istanze del servizio Cloud Foundry a un gruppo di risorse](/docs/resources?topic=resources-migrate).

## Perché non posso creare una risorsa e aggiungerla a un gruppo di risorse?
{: #create-add-resource}
{: faq}

Molto probabilmente stai avendo un problema di accesso. Devi avere almeno il ruolo di visualizzatore sul gruppo di risorse stesso e almeno il ruolo di editor sul servizio nell'account. Trova ulteriori informazioni in [Aggiunta di risorse a un gruppo di risorse](/docs/resources?topic=resources-rgs#add_to_rgs).

Per ulteriori informazioni su come controllare il tuo accesso assegnato, vedi [Controllo del tuo accesso assegnato](/docs/iam?topic=iam-iammanidaccser#review_your_access).

Se hai bisogno di accesso aggiuntivo nell'account, contatta il proprietario dell'account che è elencato nella pagina [Users](https://{DomainName}/iam#/users).

## Chi può creare i gruppi di risorse?
{: #create-resource}
{: faq}

Puoi creare dei gruppi di risorse solo se ti è stato assegnato il ruolo di Amministratore su tutti i servizi abilitati per l'accesso e l'identità {{site.data.keyword.Bluemix_notm}} nell'account.

## Posso eliminare un gruppo di risorse?
{: #delete-resource-group}
{: faq}

Non puoi eliminare un gruppo di risorse dopo averlo creato.

## Posso spostare le istanze del servizio tra i gruppi di risorse?
{: #instances-between-rgs}
{: faq}

Non puoi spostare le istanze del servizio tra i gruppi di risorse. Se assegni un'istanza del servizio in modo non corretto, devi eliminare e creare nuovamente l'istanza per assegnarla al gruppo di risorse corretto.  

## Posso visualizzare l'utilizzo del gruppo di risorse?
{: #view-usage}
{: faq}

Sì, puoi. Per aprire la pagina Dashboard di utilizzo, fai clic su **Gestisci** &gt; **Fatturazione e utilizzo**. Seleziona **Utilizzo** per visualizzare un riepilogo dell'utilizzo in base al gruppo di risorse per l'account.
