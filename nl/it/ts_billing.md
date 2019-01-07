---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Risoluzione dei problemi relativi alla gestione della fatturazione e dell'utilizzo
{: #troubleshoot}

I problemi generali con la gestione della fatturazione e dell'utilizzo possono includere l'autorizzazione richiesta di accesso alle tue informazioni di fatturazione. In molti casi, puoi risolvere questo problema seguendo pochi semplici passi.
{:shortdesc}


## Perché non posso accedere alle informazioni di fatturazione?
{: #cannot-access-billing-info}
{: troubleshoot}

Quando provi ad accedere alle informazioni di fatturazione, come ad esempio i pagamenti e le fatture, ottieni un messaggio che indica che la funzione non è disponibile.
{: tsSymptoms}

Questo accade perché non disponi dell'autorizzazione per visualizzare le informazioni di fatturazione per l'account. Devi essere un proprietario dell'account, il gestore della fatturazione dell'organizzazione Cloud Foundry oppure disporre di una politica IAM su tutti i servizi di gestione dell'account con assegnato il ruolo di amministratore.
{: tsCauses}

Puoi visualizzare le informazioni di fatturazione su qualsiasi account di cui sei il proprietario. Un gestore fatturazione può visualizzare le informazioni di fatturazione per un'organizzazione Cloud Foundry. Per le risorse abilitate a IAM, invece, devi disporre di una politica IAM su tutti i servizi di gestione dell'account con assegnato il ruolo di amministratore. 

Controlla il tuo accesso completando la seguente procedura: 

  1. Vai a **Gestisci** > **Accesso (IAM)** e seleziona **Utenti**. 
  2. Fai clic sul tuo nome dalla pagina Utenti.
  3. Fai clic su **Politiche di accesso** per visualizzare le tue politiche di accesso IAM assegnate.
  4. Fai clic su **Accesso Cloud Foundry** ed espandi le righe per le tue organizzazioni assegnate per vedere se disponi di un ruolo di Proprietario account o Gestore fatturazione.

Per ulteriori informazioni sull'accesso IAM, vedi [Ruoli Cloud IAM](/docs/iam/users_roles.html#userroles). Per ulteriori informazioni sull'accesso Cloud Foundry, invece, vedi [Ruoli Cloud Foundry](/docs/iam/cfaccess.html#cfaccess).
{: tsResolve}
