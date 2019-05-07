---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-26"

keywords: service authorization, service instance's access, connect service to app

subcollection: resources

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Connessione dei servizi a un'applicazione Cloud Foundry
{: #s2s_binding}

Per utilizzare un servizio in un'applicazione Cloud Foundry, devi creare una connessione o associare tale servizio all'applicazione.
{: shortdesc}

Per connettere un servizio alla tua applicazione partendo dalla pagina dei dettagli per un servizio specifico, completa la seguente procedura:

Puoi anche creare delle connessioni dalla tua applicazione al servizio. Seleziona la tua applicazione dall'elenco delle risorse, vai al menu **Connessioni** e seleziona il servizio.

1. Nell'elenco risorse, fai clic su **Servizi** e seleziona il servizio a cui vuoi accedere. Viene visualizzata la pagina dei dettagli del servizio.
2. Fai clic su **Connessioni** nel riquadro di navigazione.
3. Fai clic su **Crea connessione**. 
4. Fai clic su **Connetti** per la riga dell'applicazione per cui vuoi creare la connessione.
5. Seleziona un ruolo di accesso per assegnare la connessione. Questo ruolo definisce le azioni che possono essere eseguite dall'applicazione che accede al servizio.
6. Facoltativo: seleziona, crea o genera automaticamente un ID servizio per l'applicazione da utilizzare per accedere al servizio. Questo ID servizio viene assegnato al ruolo di accesso che hai selezionato nel passo precedente.
7. Facoltativo: aggiungi dei parametri di configurazione nel formato JSON.
8. Fai clic su **Collega e riprepara l'applicazione**.

Se vuoi negare alle applicazioni di accedere all'istanza del servizio dopo che sono state connesse, fai clic su **Connessioni** nel riquadro di navigazione e fai poi clic su **Annulla associazione** nel menu per l'applicazione connessa per rimuovere l'associazione al servizio.
{: tip}
