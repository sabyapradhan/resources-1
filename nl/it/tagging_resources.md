---

copyright:

  years: 2018
lastupdated: "2018-11-27"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Gestione delle tag
{: #tag}

Una tag è un'etichetta che assegni a una risorsa per filtrare facilmente le risorse nel tuo elenco risorse. Puoi utilizzare le tag per organizzare le tue risorse e trovarle facilmente in un secondo momento.  
{: shortdesc}

Per visualizzare un elenco completo delle tag nel tuo account, vai a **Gestisci > Account** e seleziona **Tag**.

## Regole e limitazioni relative alle operazioni di tag
{: #limits}

La dimensione massima di una tag è di 128 caratteri. I caratteri consentiti sono A-Z, 0-9, gli spazi vuoti, i caratteri di sottolineatura, i trattini, i punti e i caratteri due punti; le tag non sono sensibili a maiuscole/minuscole. I caratteri due punti trasformano le tag in una coppia chiave/valore (`key:value`). Non puoi utilizzare un carattere due punti in una tag senza creare una coppia chiave/valore (`key:value`). Una virgola separa le tag e, pertanto, non può essere usata all'interno del nome della tag stesso.


## Aggiunta e rimozione di tag su una risorsa
{: #add-remove}

1. Dalla console {{site.data.keyword.Bluemix_notm}}, fai clic sull'icona Menu ![Icona Menu](../icons/icon_hamburger.svg) > **Elenco risorse** per visualizzare il tuo elenco di risorse. 
2. Espandi la freccia del tipo di risorsa che contiene la risorsa su cui vuoi eseguire operazioni di tag. Ad esempio, se vuoi eseguire operazioni di tag su un'istanza di {{site.data.keyword.cos_full_notm}}, espandi **Archiviazione**.  
3. Fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per aggiungere o aggiornare una tag per la risorsa. 

    * Per aggiungere una tag, fai clic sul menu Azioni ![Menu Azioni](../icons/action-menu-icon.svg), seleziona **Aggiungi tag** e immetti un nome per la tua tag. 
    * Per aggiungere ulteriori tag, fai clic sull'icona Modifica ![Icona Modifica](../icons/edit-tagging.svg) accanto alla tag visualizzata e immetti un nome per la tua tag. Premi Invio per continuare ad aggiungere tag.
4. Per rimuovere una tag, fai clic sull'icona Modifica ![Icona Modifica](../icons/edit-tagging.svg). Fai quindi clic sull'icona Rimuovi ![Icona Rimuovi](../icons/close-tagging.svg) accanto alla tag. 

## Ricerca di tag
{: #search-tags}

Puoi cercare le tag utilizzando uno qualsiasi dei seguenti metodi:

  * Prova la barra di ricerca che si trova nella barra dei menu della console {{site.data.keyword.Bluemix_notm}}.
  * Puoi filtrare il tuo elenco risorse in base alla tag che stai cercando.
  * Dalla pagina dei dettagli dell'applicazione, puoi individuare le tag associate alla risorsa in questione.

La stessa tag può essere collegata a più risorse da vari utenti nello stesso account di fatturazione e non tutti gli utenti hanno la visibilità su tutte le risorse nell'account.
{: note}


## Operazioni di tag per i rivenditori
{: #resell}

Le tag sono visibili a tutti i membri di un account.
Se il tuo account è associato a varie organizzazioni, se sei un rivenditore ad esempio, potresti voler consigliare ai tuoi clienti di non archiviare informazioni nelle tag che potrebbero diffondere informazioni sensibili ad altri nello stesso account.

Per controllare la visibilità delle tag, fai circolare le linee guida sulle operazioni di tag e lascia che gli utenti sappiano che le tag sono visibili a livello di account. 

Utilizza dei codici invece dei nomi per clienti ed account ed evita di inserire informazioni sensibili nelle tag.
{: tip}

