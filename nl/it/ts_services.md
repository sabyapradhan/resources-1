---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-20"

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Risoluzione dei problemi relativi ai servizi
{: #services}

I problemi relativi ai servizi {{site.data.keyword.Bluemix}} potrebbero includere un errore di timeout del gateway che si verifica se elimini un'istanza del servizio. Puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

I servizi hanno diversi tipi e livelli di maturità in {{site.data.keyword.Bluemix_notm}}. Ad esempio, i servizi IBM e i servizi di terze parti e i livelli di tali servizi sono GA, beta e sperimentale. In base al tipo di servizio e al livello di maturità, potrebbero venire offerti livelli differenti di supporto. Per ulteriori informazioni, consulta [Come ottengo supporto per i servizi?](/docs/get-support/servicessupport.html#support-different-services)

## Si verifica un errore del broker di servizi quando elimini un'istanza del servizio
{: #ts_service_broker}

Potresti ricevere un messaggio di errore se tenti di eliminare un'istanza del servizio che è già stata eliminata dal controller cloud.
{:shortdesc}

Quando tenti di eliminare un'istanza del servizio, visualizzi il seguente messaggio di errore del broker dei servizi:
{: tsSymptoms}
`Timeout del gateway`

Questo problema si verifica se l'istanza del servizio è già stata eliminata dal controller cloud.
{: tsCauses}

Crea un'istanza del servizio con lo stesso nome servizio, quindi eseguine il bind alle tue applicazioni. Puoi quindi eliminare l'istanza del servizio e le applicazioni che utilizzano il servizio.   
{: tsResolve}
