---



copyright:

  years: 2017, 2018
lastupdated: "2017-12-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Gestione dell'utilizzo degli account collegati {{site.data.keyword.Bluemix_notm}}
{: #linkedusage}

Se hai un account {{site.data.keyword.Bluemix}} e SoftLayer collegato, puoi utilizzare il portale del cliente per effettuare un pagamento unico, modificare i dettagli della tua carta di pagamento e visualizzare i tuoi elementi di fatturazione e le tue fatture.
{: shortdesc}

Le opzioni di fatturazione e di utilizzo visualizzate nella console {{site.data.keyword.Bluemix_notm}} possono essere diverse se disponi di un account gratuito o se non hai un account {{site.data.keyword.Bluemix_notm}} e SoftLayer collegato.
{: tip}

## Effettuazione di un pagamento
{: #makepayment}

Puoi effettuare un pagamento unico in qualsiasi momento. Il pagamento può essere relativo all'intero saldo o a un importo parziale e i dettagli inseriti per il pagamento non vengono registrati. Completa la seguente procedura per effettuare un pagamento unico.

1. Seleziona una delle seguenti opzioni a seconda del dashboard che stai utilizzando:   
 * Dal dashboard Applicazioni o Servizi, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Effettua un pagamento**.  
 * Dal dashboard Infrastruttura, fai clic su **Account** > **Effettua un pagamento**.
3. Nel campo **Importo del pagamento**, immetti l'importo che vuoi pagare.
4. Seleziona il metodo di pagamento che preferisci:
 * Pagamento con carta di credito. Immetti i dettagli della tua carta e l'indirizzo di fatturazione della carta. Quindi, fai clic su **Effettua pagamento con carta di credito**.
 * Pagamento con PayPal. Immetti i tuoi dettagli quando viene richiesto per completare il pagamento.

Risolvi eventuali problemi segnalati con il pagamento. Il saldo dell'account viene aggiornato una volta che il pagamento è stato accettato. Puoi contattare il team di supporto facendo clic su **Supporto** > **Aggiungi ticket**.

## Modifica del metodo di pagamento
{: #changepaymethod}

Ogni account fatturabile deve avere una carta di credito registrata che sia valida. Ogni mese, la carta di credito viene addebitata in base alla quantità di utilizzo accumulata durante quel mese. Nella console {{site.data.keyword.Bluemix_notm}}, completa la seguente procedura per aggiungere o modificare i tuoi dettagli di pagamento.

1. Seleziona una delle seguenti opzioni a seconda del dashboard che stai utilizzando:  
 * Dal dashboard Applicazioni o Servizi, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Modifica metodo di pagamento**.  
 * Dal dashboard Infrastruttura, fai clic su **Account** > **Fatturazione** > **Metodo di pagamento**.
2. Nella sezione Aggiungi metodo di pagamento, immetti i dettagli della tua carta di credito e l'indirizzo di fatturazione della carta. Seleziona **Aggiungi carta di credito**.

I dettagli della tua carta vengono convalidati e quindi la carta è disponibile per l'utilizzo nel tuo account entro 24 ore. Viene inviata un'e-mail di conferma
al contatto immesso nella sezione dell'indirizzo di fatturazione della carta.

## Visualizzazione dei tuoi elementi di fatturazione
{: #viewbilling}

Puoi associare o dissociare gli elementi di fatturazione a specifici dispositivi. Per impostazione predefinita, la
pagina Elementi di fatturazione visualizza gli elementi associati. Puoi modificare la vista selezionando un'opzione
dal menu di visualizzazione. L'associazione e la dissociazione possono verificarsi per un elemento o per più di un elemento alla volta utilizzando l'operazione Azioni in blocco. I singoli elementi di fatturazione possono essere annullati in qualsiasi momento dalla pagina Elementi di fatturazione. Completa la seguente procedura per associare o dissociare i tuoi elementi di fatturazione nella console.

1. Seleziona una delle seguenti opzioni a seconda del dashboard che stai utilizzando:   
 * Dal dashboard Applicazioni o Servizi, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Fatturazione**.  
 * Dal dashboard Infrastruttura, fai clic su **Account** > **Fatturazione** > **Elementi di fatturazione**.
2. Per filtrare la vista, seleziona un'opzione di elemento di fatturazione dall'elenco.

## Visualizzazione delle tue fatture
{: #viewinvoices}

Le fatture possono essere visualizzate o pagate in qualsiasi momento. Ogni fattura viene riepilogata per Numero fattura, Data, Tipo di fattura e vari
saldi monetari. I tipi di fattura sono categorizzati come segue:

 *  Nuovo: la prima fattura in una serie di fatture ricorrenti
 *  Ricorrente: una fattura per gli addebiti ricorrenti che sono stati attivi sull'account per più di un mese
 *  Addebito una tantum: un addebito una tantum per le varie spese, che potrebbero includere dei costi aggiuntivi
 *  Credito: un credito da {{site.data.keyword.Bluemix_notm}} al saldo dell'account
 *  Rimborso: un rimborso, o un'inversione, per un addebito una tantum o ricorrente

La pagina Fatture mostra inoltre un riepilogo di fatturazione per l'account, che include il saldo corrente e la stima del saldo successivo,
il metodo di pagamento e le date dell'ultima e della prossima fattura ricorrente.

Completa la seguente procedura per visualizzare una fattura:

1. Seleziona una delle seguenti opzioni, a seconda del dashboard che stai utilizzando:  
 * Dal dashboard Applicazioni o Servizi, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Fatture**.  
 * Dal dashboard Infrastruttura, fai clic su **Account** > **Fatturazione** > **Fatture**.
2. Puoi visualizzare una fattura nel portale del cliente o scaricare la fattura.

## Utilizzo di servizi {{site.data.keyword.Bluemix_notm}} con risorse SoftLayer
{: #combined}

Puoi utilizzare facilmente servizi {{site.data.keyword.Bluemix_notm}} pubblici basati sull'API insieme alle tue risorse SoftLayer. Tutte le API sono sicure e codificate, cosicché i dati siano protetti.

Ad esempio, hai mai desiderato di aggiungere da SoftLayer capacità cognitive Watson alle tue applicazioni eseguite su server bare metal? Puoi aggiungere un servizio quale {{site.data.keyword.personalityinsightsshort}} per aiutare l'utente delle tue applicazioni in quattro passi:

1. Trova il servizio nel catalogo.
2. Fornisci un'istanza del servizio con pochi clic.
3. Imposta il servizio da eseguire con il codice esistente copiandone le credenziali e aggiungendole alla tua applicazione.
4. Effettuato l'aggiornamento nell'applicazione, distribuisci la nuova versione sulla tua infrastruttura SoftLayer.

Puoi ottenere una conoscenza di Insights and Cognitive richiamando le API Watson dalle tue applicazioni in SoftLayer per personalizzarle maggiormente. Oppure, utilizza i servizi Data and Analytics per accedere a un'analisi ad alte prestazioni per le tue applicazioni. In alternativa, selezionare un database-as-a-service in cui tu possa lasciare la gestione a {{site.data.keyword.Bluemix_notm}}.

Rinnova lo sviluppo delle tue applicazioni attraverso contenitori con servizi quali {{site.data.keyword.activedeployshort}} e {{site.data.keyword.deliverypipeline}}. Puoi quindi utilizzare il servizio {{site.data.keyword.vpn_short}} per comunicare con SoftLayer per connettere il tuo contenitore appartenente a una rete privata alla rete privata SoftLayer. Tutti gli addebiti di utilizzo dei servizi e delle risorse di calcolo sono riportati nella fattura {{site.data.keyword.Bluemix_notm}}.
