---

copyright:
  years: 2019
lastupdated: "2019-08-06"

keywords: enterprise billing, enterprise, subscription, billing unit, billing option, invoice, credit pool

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}

# Gestione centralizzata di fatturazione e utilizzo con le aziende
{: #enterprise}

Le aziende ti consentono di gestire in modo centralizzato più account {{site.data.keyword.Bluemix}}. Poiché la fatturazione è separata dai singoli account secondari e consolidata al livello aziendale, le aziende semplificano la gestione di fatturazione e pagamenti per gli account.
{: shortdesc}

Non hai familiarità con le aziende {{site.data.keyword.Bluemix_notm}}? Vedi [Cos'è un'azienda?](/docs/account?topic=account-enterprise) per ulteriori dettagli su come le aziende possono aiutarti a gestire in modo centralizzato la fatturazione e l'utilizzo.
{: tip}

## Modello di fatturazione aziendale
{: #enterprise-billing-basics}

In un'azienda, la fatturazione viene gestita dall'azienda invece che nei singoli account secondari. Questo modello di fatturazione centralizzata si differenzia da un account autonomo nei seguenti modi.

 * I crediti da tutte le sottoscrizioni o promozioni esistenti negli account aggiunti all'azienda vengono consolidati nel pool di crediti dell'azienda. L'amministratore della fatturazione aggiunge le nuove sottoscrizioni al pool di crediti dall'account aziendale.
 * L'utilizzo da tutti gli account viene dedotto dal pool di crediti condiviso. Se gli viene fornito l'accesso, gli utenti dell'azienda possono visualizzare i costi di utilizzo di tutti gli account e gruppi di account nell'azienda. Gli utenti in ogni account secondario possono continuare a monitorare l'utilizzo nello specifico account, ma non hanno la visibilità degli altri account nell'azienda.
 * L'utilizzo viene fatturato tramite l'account aziendale. Solo l'amministratore della fatturazione aziendale può visualizzare le fatture e gestire i pagamenti.

<figure>
<a href="https://{DomainName}/docs/api/content/billing-usage/images/enterprise-billing-usage.svg">
<img src="images/enterprise-billing-usage.svg" alt="Un diagramma che mostra che il credito dagli account viene aggiunto al pool di crediti aziendale, che è gestito dall'amministratore nell'account aziendale. L'accesso all'utilizzo viene gestito in modo separato e può essere destinato a un'azienda, un gruppo di account o un account."></a>
<figcaption>Figura 1. Gestione di fatturazione e utilizzo aziendali</figcaption>
</figure>

## Opzioni di fatturazione
{: #enterprise-billing-options}

Le aziende richiedono la fatturazione di sottoscrizione, che significa che acquisti una sottoscrizione per l'ammontare di crediti che spendi durante il termine di sottoscrizione e l'utilizzo viene dedotto dal credito di sottoscrizione ad una tariffa scontata. L'account che utilizzi per creare l'azienda deve essere un [account Sottoscrizione](/docs/account?topic=account-accounts#subscription-account). Dopo aver creato l'azienda, puoi aggiungere qualsiasi tipo di account all'azienda. Se aggiungi un account Lite o di prova, ne viene automaticamente eseguito l'upgrade a un account Pagamento a consumo.

Alcuni account Pagamento a consumo non possono essere importati direttamente in un'azienda, come molti account Pagamento a consumo che sono fatturati in dollari americani (USD). Tuttavia, puoi ancora importare questi account nella tua azienda convertendoli in account Sottoscrizione e poi importandoli. Per convertire un account, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).
{: note}

Ogni azienda supporta una sola valuta di fatturazione. Tutti gli account devono utilizzare la valuta di fatturazione aziendale prima di aggiungerli all'azienda. Gli account esistenti che vengono importati nell'azienda non possono più gestire in modo separato la propria fatturazione. Di conseguenza, il credito di sottoscrizione non può essere aggiunto a singoli account secondari. Il credito di sottoscrizione deve essere aggiunto all'account aziendale, dove diventa parte del pool di crediti aziendale.

### Fatturazione della transizione quando aggiungi degli account
{: #billing-transition}

Quando aggiungi un account esistente a un'azienda, la sua fatturazione delle transizioni viene gestita dall'account aziendale. Questa transizione include le seguenti modifiche all'account.

   * Per gli account Sottoscrizione che vengono aggiunti, il tipo di account viene modificato con Pagamento a consumo. Questa modifica rispecchia il fatto che l'account non ha le proprie sottoscrizioni, ma ha ancora accesso completo ai servizi fatturabili e pronti per la produzione.
   * Le sottoscrizioni e le promozioni da ogni account vengono spostate all'account aziendale, dove diventano parte del pool di crediti. Dopo lo spostamento, ciascuna sottoscrizione ha gli stessi credito rimanente e periodo di termine, ma gli viene fornito un nuovo ID univoco.
   * L'accesso alle informazioni di fatturazione e pagamento per i successivi periodi di fatturazione è limitato agli utenti nell'account aziendale. Gli utenti in un account secondario non possono accedere alle informazioni di fatturazione e pagamento, ad esempio le fatture, i pagamenti o le sottoscrizioni, anche se precedentemente ne avevano accesso nell'account. Per visualizzare o gestire la fatturazione, gli utenti devono essere invitati nell'account aziendale e gli deve essere dato l'accesso al servizio di fatturazione in tale account.
   * L'utilizzo viene fatturato dall'account aziendale per l'intero mese quando è stato aggiunto l'account. Ad esempio, se aggiungi un account all'azienda il 15 giugno, tutto l'utilizzo del mese di giugno viene rispecchiato nella fattura di luglio.

### Pool di crediti condiviso
{: #credit-pool}

Il pool di crediti aziendale consolida i crediti da tutti gli account nell'azienda e li condivide con gli account. Il pool include i crediti da tutte le origini, inclusi il credito di sottoscrizione della piattaforma, il credito promozionale e il credito di supporto. Quando gli account nell'azienda creano e utilizzano le risorse, il costo di questo utilizzo viene dedotto dal pool di crediti.

L'amministratore della fatturazione nell'account aziendale può visualizzare e monitorare l'importo totale del credito disponibile nel dashboard aziendale. Se è necessario ulteriore credito per coprire l'utilizzo dell'azienda, può essere acquistata una nuova sottoscrizione e poi aggiunta all'account aziendale. Le sottoscrizioni possono essere aggiunte solo all'account aziendale e non possono essere aggiunte ad altri account nell'azienda.

Poiché le sottoscrizioni possono essere dimensionate per l'intera azienda invece che per account, hai i seguenti vantaggi:
   * Dimensionamento della sottoscrizione più semplice perché le sottoscrizioni si applicano a più di un account
   * Sconti migliori sui costi di utilizzo perché le sottoscrizioni sono più grandi
   * Meno date di scadenza di cui tenere traccia e da gestire dopo la scadenza delle sottoscrizioni esistenti

In un'azienda, le sottoscrizioni sono gestire dall'account aziendale nello stesso modo di un account autonomo. Vedi [Gestione delle sottoscrizioni](/docs/billing-usage?topic=billing-usage-subscriptions) per ulteriori informazioni sulla gestione delle tue sottoscrizioni di piattaforma e supporto.

## Report sull'utilizzo
{: #enterprise-usage-reporting}

Le aziende forniscono il report dell'utilizzo dall'alto verso il basso in modo che puoi tenere traccia dei costi dell'utilizzo delle risorse da tutti gli account nell'azienda. A partire dal livello aziendale, puoi navigare all'interno della struttura aziendale per vedere i costi di utilizzo stimati all'interno di ogni account o gruppo di account. Al livello dell'account, gli utenti aziendali possono visualizzare i costi per ogni tipo di risorsa o servizio nell'account.

Gli amministratori aziendali possono fornire l'accesso granulare agli utenti in modo che possano visualizzare l'utilizzo solo per alcuni gruppi di account o account. Ad esempio, diciamo che la tua azienda ha dei gruppi di account per ogni dipartimento e ogni dipartimento ha dei gruppi di accesso per ogni team.
   * Fornisci al tuo direttore finanziario l'accesso per visualizzare l'intera azienda in modo che possa tenere traccia e recuperare i costi da ogni dipartimento.
   * Fornisci ad ogni responsabile del dipartimento l'accesso per visualizzare l'intero utilizzo del gruppo di account del proprio dipartimento.
   * Fornisci ad ogni responsabile del team l'accesso per visualizzare solo gli account del gruppo di account del proprio team.

Poiché l'accesso nell'azienda è separato dall'accesso in ogni account, gli utenti aziendali non possono automaticamente gestire le risorse all'interno degli account secondari. In modo simile, gli utenti in ogni account possono continuare a visualizzare il proprio utilizzo corrente e passato dalla pagina degli utilizzi indipendentemente dal fatto che dispongono dell'accesso all'azienda.

Puoi visualizzare l'utilizzo dalla pagina Utilizzo nella console, dalla CLI o dall'API Enterprise Usage Reports. Per ulteriori informazioni, vedi [Visualizzazione dell'utilizzo in un'azienda](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Fatturazione e pagamenti
{: #enterprise-invoicing}

L'utilizzo nell'azienda viene fatturato tramite l'account aziendale.  Come per gli account fatturabili, l'utilizzo viene fatturato su una base mensile e la fattura deve essere pagata alla data di fatturazione del tuo account. Durante ogni ciclo di fatturazione, viene resa disponibile una sola fattura con i costi di utilizzo da tutti gli account nell'account aziendale. La fattura contiene i costi di tutto l'utilizzo di piattaforma e infrastruttura come un elemento a singola riga nella tua fattura. Se vengono utilizzati tutti i crediti nel pool di crediti, la fattura contiene un elemento riga per ogni spesa eccedente.

Poiché tutto l'utilizzo viene fatturato tramite l'account aziendale, gli account secondari all'interno dell'azienda non ricevono fatture separate.

Puoi analizzare i costi di utilizzo per ogni account o gruppo di account sulla pagina Utilizzo nell'account aziendale. Per i dettagli, vedi [Visualizzazione dell'utilizzo in un'azienda](/docs/billing-usage?topic=billing-usage-enterprise-usage).
{: tip}

## Gestione dell'accesso per la fatturazione e l'utilizzo aziendali
{: #enterprise-billing-access}

Come per gli altri ruoli di gestione aziendali, l'accesso alla fatturazione e all'utilizzo aziendali viene gestito tramite l'account aziendale. Gli utenti devono essere invitati nell'account aziendale e gli deve essere assegnata una politica di accesso con un ruolo sul servizio pertinente.

In un'azienda, gli accessi alla fatturazione e all'utilizzo vengono assegnati separatamente.

   * L'accesso alla fatturazione viene fornito assegnando agli utenti aziendali un ruolo sul servizio di fatturazione. Ad esempio, puoi assegnare il ruolo di visualizzatore a un utente aziendale in modo che può visualizzare la quantità di crediti di sottoscrizione disponibili nel pool di crediti oppure puoi assegnare il ruolo di editor o amministratore in modo che può aggiungere nuove sottoscrizioni o gestire i metodi di pagamento.
   * L'accesso all'utilizzo viene fornito assegnando agli utenti aziendali il ruolo di amministratore, editor o visualizzatore dei report di utilizzo sul servizio aziendale. Puoi assegnare questo accesso per l'intera azienda o per gruppi di account o account specifici.

Se vuoi che l'amministratore della fatturazione possa visualizzare i costi per account o gruppo di account, assicurati di assegnargli l'accesso appropriato sia al servizio aziendale che di fatturazione.
{: tip}

Per ulteriori informazioni, vedi [Gestione di utenti e accesso per le aziende](/docs/iam?topic=iam-enterprise-access).
