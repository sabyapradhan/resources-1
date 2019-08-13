---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-05"

keywords: service endpoint, private network endpoint, connect service to private network

subcollection: resources

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:download: .download}

# Accesso sicuro ai servizi utilizzando gli endpoint del servizio
{: #service-endpoints}

Ai clienti che utilizzano i servizi basati sul cloud per i carichi di lavoro di produzione viene richiesta una maggiore attenzione alla sicurezza. Per molti clienti, l'accesso ai servizi in modo sicuro non è solo una politica aziendale sensata ma, in alcuni casi, è richiesto dai regolamenti di conformità, {{site.data.keyword.IBM_notm}} ha migliorato le opzioni di connettività per i clienti che richiedono delle opzioni di connettività isolata per i loro carichi di lavoro. 

Con gli endpoint del servizio {{site.data.keyword.cloud}}, puoi stabilire una connessione ai servizi {{site.data.keyword.cloud_notm}} sulla rete privata {{site.data.keyword.cloud_notm}}. Lo spostamento di questi carichi di lavoro dalla rete pubblica offre due vantaggi:

* I servizi non sono più serviti su un indirizzo IP instradabile su internet. Sta diventando sempre più frequente che i consumatori del cloud desiderino un accesso limitato o nessun accesso a internet pubblico dai loro servizi. Ora, con la funzione di endpoint del servizio, i team dei servizi possono creare un'interfaccia sulla rete privata per i loro servizi che i clienti possono utilizzare per connettersi. L'accesso a Internet non è più un requisito per stabilire una connessione ai servizi {{site.data.keyword.cloud_notm}}.
* Non sono previsti addebiti di larghezza di banda fatturabili o misurati sulla rete privata. In passato, ti veniva addebitata in fattura la larghezza di banda in uscita quando comunicavi con un servizio {{site.data.keyword.cloud_notm}}. 

La seguente figura mostra come viene instradato il traffico tramite la rete privata di {{site.data.keyword.cloud_notm}} quando si accede ai servizi cloud tramite gli endpoint del servizio.

![Endpoint del servizio IBM Cloud](images/CSE.png "Traffico instradato tramite un endpoint del servizio")

Per utilizzare gli endpoint del servizio {{site.data.keyword.cloud_notm}}, devi abilitare VRF (virtual routing and forwarding) nel tuo account.  Puoi quindi abilitare l'uso degli endpoint del servizio. Dopo che sono state abilitate entrambe le opzioni, puoi iniziare a creare dei servizi che supportano l'uso di VRF e degli endpoint del servizio dal catalogo. Per ulteriori informazioni, vedi [Abilitazione di VRF e degli endpoint del servizio](/docs/account?topic=account-vrf-service-endpoint).
