---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: service availability, service location, using services across regions

subcollection: resources

---

{:shortdesc: .shortdesc}

# Utilizzo dei servizi in un'altra regione
{: #cross_region_service}

Se disponi di un'istanza di servizio creata e associata mediante bind ad applicazioni in un'unica regione, puoi utilizzare questa istanza in un'altra regione utilizzando uno dei seguenti metodi:
{: shortdesc}

  * Utilizza le credenziali del servizio per configurare direttamente l'istanza della tua applicazione. Per i dettagli, vedi [Connessione dei servizi alle applicazioni esterne](/docs/resources?topic=resources-externalapp#externalapp).
  * Crea come ponte un servizio fornito dall'utente.

	Per utilizzare un'istanza del servizio che si trova
in un'altra regione, completa la seguente procedura:

      1. Per passare alla regione in cui si trova l'istanza del servizio, fai clic sull'**icona Menu  ![Icona Menu](../icons/icon_hamburger.svg)** > **Elenco risorse**. Espandi quindi il menu **UBICAZIONE** e seleziona la regione.

      2. Recupera le credenziali e i parametri di connessione dalla variabile di ambiente VCAP_SERVICES dell'istanza del servizio nella regione in cui si trova il servizio. Completa la seguente
procedura:

	       1. Nel dashboard {{site.data.keyword.Bluemix_notm}}, fai clic su **Visualizza tutto** sul tile delle tue applicazioni. Viene visualizzata la pagina Panoramica.
	       2. Nel riquadro di navigazione, fai clic su **Credenziali**. Vengono visualizzati i dettagli della variabile di ambiente *VCAP_SERVICES*. Registra il contenuto JSON per l'istanza
del servizio.

      3. Passa alla regione in cui desideri utilizzare l'istanza del
servizio. Fai clic sull'**icona Menu ![Icona Menu](../icons/icon_hamburger.svg)** > **Elenco risorse**. Espandi quindi il menu **UBICAZIONE** e seleziona la regione dove vuoi usare l'istanza del servizio.

      4. Crea un'istanza del servizio fornito dall'utente utilizzando le credenziali
e i parametri di connessione che hai registrato dalla variabile di ambiente
*VCAP_SERVICES*.

      5. Esegui il bind dell'istanza del servizio fornito dall'utente alla tua applicazione
utilizzando il seguente comando:

	     ```
	     ibmcloud service bind myapp user-provided_service_instance
	     ```
