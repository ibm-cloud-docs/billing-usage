---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-11"

keywords: troubleshoot billing, billing error, payment error, error message, feature code, subscription code

subcollection: billing-usage

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

Quando provi ad accedere alle tue informazioni di fatturazione, come ad esempio i pagamenti e le fatture, ottieni un messaggio che indica che la funzione non è disponibile.
{: tsSymptoms}

Otterrai questo messaggio perché non disponi dell'autorizzazione per visualizzare le informazioni di fatturazione per l'account. Devi essere un proprietario dell'account, il gestore della fatturazione dell'organizzazione Cloud Foundry oppure disporre di una politica IAM su tutti i servizi di gestione dell'account con assegnato il ruolo di amministratore.
{: tsCauses}

Puoi visualizzare le informazioni di fatturazione su qualsiasi account di cui sei il proprietario. Un gestore fatturazione può visualizzare le informazioni di fatturazione per un'organizzazione Cloud Foundry. Per le risorse abilitate a IAM, invece, devi disporre di una politica IAM su tutti i servizi di gestione dell'account con assegnato il ruolo di amministratore.

Controlla il tuo accesso completando la seguente procedura:

  1. Vai a **Gestisci > Accesso (IAM)** e seleziona **Utenti**.
  2. Fai clic sul tuo nome dalla pagina Utenti.
  3. Fai clic su **Politiche di accesso** per visualizzare le tue politiche di accesso IAM assegnate.
  4. Fai clic su **Accesso Cloud Foundry** ed espandi le righe per le tue organizzazioni assegnate per vedere se disponi di un ruolo di Proprietario account o Gestore fatturazione.

Per ulteriori informazioni sull'accesso IAM, vedi [Ruoli Cloud IAM](/docs/iam?topic=iam-userroles). Per ulteriori informazioni sull'accesso Cloud Foundry, invece, vedi [Ruoli Cloud Foundry](/docs/iam?topic=iam-cfaccess).
{: tsResolve}


## Perché non posso applicare un codice funzione?
{: #cannot-apply-feature-code}
{: troubleshoot}

Quando tenti di applicare un codice funzione, visualizzi un errore che indica che il codice non può essere applicato.
{: tsSymptoms}

Il tuo account non soddisfa i requisiti per il codice funzione o non hai il livello di accesso richiesto nell'account.
{: tsCauses}

- Verifica di avere il tipo di account corretto. Ad esempio, alcuni codici funzione per le promozioni didattiche sono previsti solo per gli account Lite. Per visualizzare il tipo del tuo account, vai a **Gestisci > Account** e seleziona **Impostazioni account**. Per i dettagli, vedi [Applicazione di codici funzione](/docs/account?topic=account-codes).
- Verifica di disporre dell'accesso per applicare il codice funzione. Per applicare qualsiasi codice funzione, devi avere un ruolo di Editor o superiore su tutti i servizi di gestione account. Per esaminare o modificare i ruoli, vedi [Assegnazione dell'accesso ai servizi di gestione dell'account](/docs/iam?topic=iam-account-services).
{: tsResolve}
