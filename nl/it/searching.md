---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-30"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}


# Ricerca delle risorse
{: #searching-for-resources}

Puoi cercare le risorse di cui è stato eseguito il provisioning che prevedi di trovare nell'elenco risorse e nelle offerte nel catalogo da dovunque tu sia nella console {{site.data.keyword.cloud}}. Immetti la risorsa o la tag nel campo di ricerca dalla barra dei menu della console. Puoi anche utilizzare la CLI (command-line interface) di {{site.data.keyword.Bluemix_notm}} per cercare nelle tue risorse. La CLI cerca applicazioni distribuite e istanze del servizio in tutte le ubicazioni e in tutti i data center.
{:shortdesc}

## Perfezionamento dei tuoi risultati della ricerca
{: #results}

<dl>
<dt>Visualizza tutti i risultati delle risorse</dt>
<dd>Utilizza questa opzione per visualizzare un elenco risorse filtrato che compila automaticamente il campo del nome all'interno dell'elenco risorse, dandoti i risultati più pertinenti. La ricerca restituita visualizza i primi 10 risultati delle risorse. Se sai che ci sono più risultati, puoi visualizzarli tutti dall'elenco risorse. Questa opzione viene visualizzata se corrisponde a un risultato della risorsa o a una ricerca di tag. Se non corrisponde a un nome o a una tag di risultato delle risorse, non viene visualizzata.</dd>
<dt>Visualizza tutti i risultati del catalogo</dt>
<dd>Utilizza questa opzione per visualizzare una ricerca nel catalogo filtrata. I primi cinque risultati vengono visualizzati in base al nome. Se vuoi dei criteri di ricerca più dettagliati per le voci di catalogo, come ad esempio la ricerca nella descrizione, puoi fare clic su questo link e ottenere una vista dei risultati del catalogo filtrata. Questa opzione ti aiuta a trovare le offerte che vuoi creare più rapidamente. Viene visualizzata se corrisponde a un risultato del catalogo. Questo campo non viene visualizzato se la tua query di ricerca inizia con `tag:`.</dd>
<dt>Ricerca nei casi di supporto</dt>
<dd>Utilizza questa opzione per filtrare in base ai tuoi casi di supporto aperti nella piattaforma, comprese le risorse dell'infrastruttura. Viene visualizzata alla fine della ricerca se cerchi qualcosa, anche se cerchi in base alla `tag:`.</dd>
<dt>Ricerca nei documenti</dt>
<dd>Utilizza questa opzione per ottenere una vista filtrata della documentazione. Viene visualizzata alla fine della ricerca se cerchi qualcosa, anche se cerchi in base alla `tag:`.</dd>
</dl>

Premi il tasto barra (/) per portare il tuo cursore al campo di ricerca.
{: tip}


## Ricerca con la CLI
{: #searching-cl}

Puoi anche cercare in tutte le tue risorse utilizzando la sintassi di query Lucene, con un singolo comando utilizzando la CLI {{site.data.keyword.Bluemix_notm}}, a partire dalla versione 0.6.7. 

  La CLI attualmente non cerca le risorse in esecuzione sulle istanze dell'infrastruttura classica.
  {: note}

Puoi cercare i seguenti attributi: 

<dl>
<dt>` name `</dt>
<dd> Il nome definito dall'utente della risorsa.</dd>
<dt>`regione`</dt>
<dd>L'ubicazione geografica dove viene eseguito il provisioning della risorsa. I valori consentiti sono `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de` e `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>Il nome del servizio come si presenta nella colonna Name dell'output di 'ibmcloud catalog service-marketplace'.</dd>
<dt>`family`</dt>
<dd>Il componente cloud a cui appartiene la tua risorsa. I valori consentiti sono `cloud_foundry`, `containers` o `resource_controller`.</dd>
<dt>`organization_id`</dt>
<dd>Il GUID organizzazione Cloud Foundry.</dd>
<dt>`doc.space_id`</dt>
<dd>Il GUID spazio Cloud Foundry.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>L'ID del gruppo di risorse.</dd>
<dt>`type`</dt>
<dd>Il tipo di risorsa. I valori consentiti sono `k8-cluster`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding` e `resource-group`.</dd>
<dt>`creation_date`</dt>
<dd>La data in cui viene creata la risorsa.</dd>
<dt>`modification_date`</dt>
<dd> La data dell'ultima modifica della risorsa.</dd>
</dl>

### Esempi di ricerca
{: #resource-name}

I seguenti esempi possono aiutarti a cercare le risorse dell'account.

* Per cercare tutte le tue risorse denominate `ABC`, immetti il seguente comando.

    `ibmcloud resource search ‘name:ABC’`

* Per cercare tutte le applicazioni Cloud Foundry denominate `MyResource`, immetti il seguente comando.

    `ibmcloud resource search 'name:my* AND type:cf-application'
`

* Per cercare tutte le istanze del servizio di Message Hub, immetti il seguente comando.

    `ibmcloud resource search 'service_name:messagehub'`

* Per cercare tutte le risorse nell'organizzazione Cloud Foundry `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` o nel gruppo di risorse `c900d9671b235c00461c5e311a8aeced` nella regione `us-south`, immetti il seguente comando.

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* Per cercare tutte le risorse create tra il 16 maggio 2018 e il 20 maggio 2018, immetti il seguente comando.

    `ibmcloud resource search "creation_date:[2018-05-16T00:00:00Z TO 2018-05-20T00:00:00Z]"`
    
* Per cercare tutte le risorse il cui nome inizia con "my", ordinate in base al tipo, immetti il seguente comando.

    `ibmcloud resource search 'name:my*' -s type`


