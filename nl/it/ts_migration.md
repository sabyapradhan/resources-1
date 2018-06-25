---

copyright:

  years: 2018

lastupdated: "2018-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Risoluzione dei problemi relativi alla migrazione delle istanze del servizio

Se riscontri dei problemi durante la migrazione un'istanza del servizio Cloud Foundry a un gruppo di risorse, esamina i seguenti problemi comuni per aiutarti a procedere con la migrazione.

## Cosa succede se ho migrato la mia istanza del servizio nel gruppo di risorse sbagliato?

Attualmente, non puoi spostare le risorse tra i gruppi di risorse dopo che sono state assegnate. Quindi, se hai migrato un'istanza nel gruppo di risorse sbagliato, puoi provare ad eliminare l'istanza e a crearne una nuova dal catalogo. Puoi assegnare l'istanza al gruppo di risorse corretto mentre la stai creando.

## Perché non riesco ad eseguire la migrazione?

Potresti non disporre dell'accesso corretto per migrare un'istanza del servizio. Per ulteriori informazioni, consulta [Chi può migrare le istanze del servizio](/docs/account/instance_migration.html#whocanmigrate).

## Perché non tutti i miei servizi sono idonei per la migrazione?

Attualmente, non tutti i servizi sono disponibili per essere gestiti utilizzando il controllo dell'accesso IAM e i gruppi di risorse. Se disponi dell'accesso per completare l'attività di migrazione, riceverai una notifica quando i servizi abilitano l'utilizzo di IAM.
