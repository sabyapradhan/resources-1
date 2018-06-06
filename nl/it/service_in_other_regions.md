---

copyright:
  years: 2015, 2018
lastupdated: "2018-01-16"

---

{:shortdesc: .shortdesc}

# Utilizzo dei servizi in un'altra regione
{: #cross_region_service}

Se disponi di un'istanza di servizio creata e associata mediante bind ad applicazioni in un'unica regione, puoi utilizzare questa istanza in un'altra regione utilizzando uno dei seguenti metodi:
{: shortdesc}

  * Utilizza le credenziali del servizio per configurare direttamente l'istanza della tua applicazione. Per i dettagli, vedi [Abilitazione di applicazioni esterne all'utilizzo dei servizi {{site.data.keyword.Bluemix_notm}}](/docs/apps/reqnsi.html#accser_external){: new_window}.
  * Crea come ponte un servizio fornito dall'utente.

	Per utilizzare un'istanza del servizio che si trova
in un'altra regione, completa la seguente procedura:

      1. Passa alla regione in cui si trova l'istanza del servizio. Nella barra dei menu di {{site.data.keyword.Bluemix_notm}}, espandi il menu **Regione** e quindi seleziona la regione in cui si trova l'istanza del servizio.

      2. Recupera le credenziali e i parametri di connessione dalla variabile di ambiente VCAP_SERVICES dell'istanza del servizio nella regione in cui si trova il servizio. Completa la seguente
procedura:

	       1. Nel Dashboard {{site.data.keyword.Bluemix_notm}}, fai clic sul tile dell'applicazione. Viene visualizzata la pagina Panoramica.
	       2. Nel riquadro di navigazione, fai clic su **Credenziali**. Vengono visualizzati i dettagli della variabile di ambiente *VCAP_SERVICES*. Registra il contenuto JSON per l'istanza
del servizio.

      3. Passa alla regione in cui desideri utilizzare l'istanza del
servizio. Nella barra dei menu di {{site.data.keyword.Bluemix_notm}}, espandi il menu **Regione** e quindi seleziona la regione in cui vuoi utilizzare l'istanza del servizio.

      4. Crea un'istanza del servizio fornito dall'utente utilizzando le credenziali
e i parametri di connessione che hai registrato dalla variabile di ambiente
*VCAP_SERVICES*. Per informazioni su come creare un'istanza
del servizio fornito dall'utente, vedi [Creazione di un'istanza
del servizio fornito dall'utente](/docs/apps/reqnsi.html#user_provide_services).

      5. Esegui il bind dell'istanza del servizio fornito dall'utente alla tua applicazione
utilizzando il seguente comando:

	     ```
	     bluemix service bind myapp user-provided_service_instance
	     ```
