---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-26"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Risoluzione dei problemi relativi ai servizi e alle risorse
{: #services}

I problemi con il servizio {{site.data.keyword.Bluemix}} possono includere problemi con l'eliminazione delle istanze del servizio. Puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Perché non posso eliminare la mia istanza del servizio? 
{: #ts_service_broker}

Potresti ricevere un messaggio di errore se tenti di eliminare un'istanza del servizio che è già stata eliminata dal controller cloud.
{:shortdesc}

Quando tenti di eliminare un'istanza del servizio, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`Timeout del gateway`

Questo problema si verifica se l'istanza del servizio è già stata eliminata dal controller cloud.
{: tsCauses}

Crea un'istanza del servizio con lo stesso nome servizio ed eseguine il bind alle tue applicazioni. Puoi quindi eliminare l'istanza del servizio e le applicazioni che utilizzano il servizio.   
{: tsResolve}
