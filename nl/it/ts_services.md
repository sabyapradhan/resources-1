---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-23"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Risoluzione dei problemi relativi ai servizi e alle risorse
{: #services}

I problemi generali con i servizi e le risorse possono includere dei problemi con l'eliminazione di istanze del servizio o con la migrazione dei servizi. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Perché non posso eliminare la mia istanza del servizio?
{: #ts_service_broker}
{: troubleshoot}

Potresti ricevere un messaggio di errore se tenti di eliminare un'istanza del servizio che è già stata eliminata dal controller cloud.
{:shortdesc}

Quando tenti di eliminare un'istanza del servizio, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`Timeout del gateway`

Questo problema si verifica se l'istanza del servizio è già stata eliminata dal controller cloud.
{: tsCauses}

Crea un'istanza del servizio con lo stesso nome servizio ed eseguine il bind alle tue applicazioni. Puoi quindi eliminare l'istanza del servizio e le applicazioni che utilizzano il servizio.   
{: tsResolve}

## Perché un'istanza del servizio è stata migrata al gruppo di risorse errato? 
{: #ts_service_instance}
{: troubleshoot}

Potresti notare che un'istanza del servizio è stata migrata al gruppo di risorse errato e non è possibile riassegnarla.
{:shortdesc}

Non puoi spostare le risorse tra i gruppi di risorse dopo che sono state assegnate.
{: tsSymptoms}

Hai assegnato l'istanza al gruppo di risorse errato.  
{: tsCauses}

Per correggere questo problema, puoi provare a eliminare l'istanza e a crearne una nuova dal catalogo. Puoi assegnarla al gruppo di risorse corretto quando crei la nuova istanza.
{: tsResolve}

## Perché non posso migrare un'istanza idonea?
{: #ts_migrate_instance}
{: troubleshoot}

In quanto utente nell'account, stai avendo problemi quando migri un'istanza idonea.
{:shortdesc}

Non riesci a migrare un'istanza idonea.
{: tsSymptoms}

Se non riesci a migrare un'istanza idonea, è possibile che tu non disponga dell'accesso corretto.
{: tsCauses}

Gli utenti devono avere un accesso specifico per migrare un'istanza. Per controllare qual è l'accesso di cui disponi, fai clic su **Gestisci** &gt; **Access (IAM)** dalla barra dei menu della console e fai quindi clic su **Utenti**. Fai clic sul tuo nome ed esamina le tue Politiche di accesso per i ruoli IAM assegnati e Accesso Cloud Foundry per visualizzare quali sono le organizzazioni a cui hai accesso e i tuoi ruoli Cloud Foundry assegnati.
{: tsResolve}

## Perché non posso migrare tutti i miei servizi?
{: #ts_service_migration}
{: troubleshoot}

Non tutti i servizi sono idonei per la migrazione.
{:shortdesc}

Non riesci a migrare determinati servizi.
{: tsSymptoms}

Stai migrando dei servizi che non sono disponibili per essere aggiunti ai gruppi di risorse e non sono gestiti utilizzando IAM (Identity and Access Management). Se un servizio non è idoneo, non c'è un'opzione per la migrazione.
{: tsCauses}

Controlla i servizi per confermare che sono idonei per la migrazione. Ricevi una notifica e vedi un indicatore `support_rc_migration` che indica se un servizio è idoneo per la migrazione.
{: tsResolve}
