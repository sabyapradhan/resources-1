---

copyright:

  years: 2018

lastupdated: "2018-07-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Risoluzione dei problemi relativi alla migrazione delle istanze del servizio

Se riscontri dei problemi durante la migrazione di un'istanza del servizio Cloud Foundry a un gruppo di risorse, esamina i seguenti problemi comuni per aiutarti a procedere.

## Un'istanza del servizio è stata migrata al gruppo di risorse sbagliato

Non puoi spostare le risorse tra i gruppi di risorse dopo che sono state assegnate. Quindi, se hai assegnato un'istanza al gruppo di risorse sbagliato, puoi provare a eliminare l'istanza e a crearne una nuova dal catalogo. Puoi assegnare l'istanza al gruppo di risorse corretto durante la sua creazione.

## Un utente nell'account non può migrare un'istanza idonea

È possibile che non ti sia stato assegnato l'accesso corretto per migrare un'istanza del servizio. Per ulteriori informazioni, vedi [Chi può migrare le istanze del servizio?](/docs/resources/instance_migration.html#whocanmigrate).

## Non tutti i servizi sono idonei per la migrazione

Non tutti i servizi sono disponibili per essere aggiunti ai gruppi di risorse e gestiti tramite Identity and Access Management. Se disponi dell'accesso per completare l'attività di migrazione, riceverai una notifica quando i servizi saranno idonei.
