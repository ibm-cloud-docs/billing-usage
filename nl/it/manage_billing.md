---



copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Gestione dell'utilizzo degli account collegati {{site.data.keyword.Bluemix_notm}}
{: #linkedusage}

Se hai un account {{site.data.keyword.Bluemix}} e SoftLayer collegato, puoi utilizzare il portale clienti per effettuare un pagamento unico, modificare i dettagli della tua carta di pagamento e visualizzare i tuoi elementi di fatturazione e le tue fatture.
{: shortdesc}

Le opzioni di fatturazione e di utilizzo visualizzate nella console {{site.data.keyword.Bluemix_notm}} possono essere diverse se disponi di un account Lite o se non hai un account collegato.
{: tip}

## Effettuazione di un pagamento
{: #makepayment}

Puoi effettuare un pagamento unico in qualsiasi momento. Il pagamento può essere relativo all'intero saldo o a un importo parziale. I dettagli inseriti per il pagamento non vengono registrati. Completa la seguente procedura per effettuare un pagamento unico:

1. Dalla barra dei menu, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Effettua un pagamento**.  
2. Nel campo **Importo del pagamento**, immetti l'importo che vuoi pagare.
3. Seleziona il metodo di pagamento che preferisci:
 * Pagamento con carta di credito. Immetti i dettagli della tua carta e l'indirizzo di fatturazione della carta. Quindi, fai clic su **Effettua pagamento con carta di credito**.
 * Pagamento con PayPal. Immetti i tuoi dettagli quando viene richiesto per completare il pagamento.

Risolvi eventuali problemi segnalati con il pagamento. Il saldo dell'account viene aggiornato una volta che il pagamento è stato accettato. Puoi contattare il team di supporto facendo clic su **Supporto** > **Aggiungi ticket**.

## Modifica del metodo di pagamento
{: #changepaymethod}

Ogni account fatturabile deve avere una carta di credito registrata che sia valida. Ogni mese, la carta di credito viene addebitata in base alla quantità di utilizzo accumulata durante quel mese. Nella console {{site.data.keyword.Bluemix_notm}}, completa la seguente procedura per aggiungere o modificare i tuoi dettagli di pagamento:

1. Dalla barra dei menu, fai clic su **Gestisci** > **Fatturazione e utilizzo** > **Modifica metodo di pagamento**.  
2. Nella sezione Aggiungi metodo di pagamento, immetti i dettagli della tua carta di credito e l'indirizzo di fatturazione della carta. Seleziona **Aggiungi carta di credito**.

I dettagli della tua carta vengono convalidati e quindi la carta è disponibile per l'utilizzo nel tuo account entro 24 ore. Viene inviata un'e-mail di conferma
al contatto immesso nella sezione dell'indirizzo di fatturazione della carta.

## Visualizzazione dei tuoi elementi di fatturazione
{: #viewbilling}

Puoi associare o annullare l'associazione degli elementi di fatturazione da un dispositivo specifico. Per impostazione predefinita, la pagina **Elementi di fatturazione** visualizza gli elementi associati. Puoi modificare la vista selezionando un'opzione
dal menu di visualizzazione. Puoi associare o annullare l'associazione di un elemento o utilizzare l'operazione Azioni in blocco per associare o annullare l'associazione di più elementi alla volta. Puoi inoltre annullare singoli elementi di fatturazione in qualsiasi momento. 

1. Seleziona l'opzione **icona Menu ![icona Menu](../icons/icon_hamburger.svg) > Infrastruttura**. 
2. Dalla barra dei menu, fai clic su **Account** > **Fatturazione** > **Elementi di fatturazione**.
3. Per filtrare la vista, seleziona un'opzione di elemento di fatturazione dall'elenco.

## Visualizzazione delle tue fatture
{: #viewinvoices}

Puoi visualizzare o pagare le tue fatture in qualsiasi momento. Ogni fattura viene riepilogata per Numero fattura, Data, Tipo di fattura e vari
saldi monetari. I tipi di fattura sono descritti nel seguente elenco:

 *  Nuovo: la prima fattura in una serie di fatture ricorrenti
 *  Ricorrente: una fattura per gli addebiti ricorrenti che sono attivi sull'account per più di un mese
 *  Addebito una tantum: un addebito una tantum per le varie spese, che potrebbero includere dei costi aggiuntivi
 *  Credito: un credito da {{site.data.keyword.Bluemix_notm}} al saldo dell'account
 *  Rimborso: un rimborso, o un'inversione, per un addebito una tantum o ricorrente

La pagina **Fatture** mostra inoltre un riepilogo di fatturazione per l'account, che include il saldo corrente e la stima del saldo successivo,
il metodo di pagamento e le date dell'ultima e della prossima fattura ricorrente.

Completa la seguente procedura per visualizzare una fattura:

1. Seleziona l'opzione **icona Menu ![icona Menu](../icons/icon_hamburger.svg) > Infrastruttura**. 
2. Dalla barra dei menu, fai clic su **Account** > **Fatturazione** > **Fatture**.
3. Puoi visualizzare una fattura nel portale clienti o scaricare la fattura.

## Utilizzo di servizi {{site.data.keyword.Bluemix_notm}} con risorse SoftLayer
{: #combined}

Puoi utilizzare facilmente servizi {{site.data.keyword.Bluemix_notm}} pubblici basati sull'API insieme alle tue risorse SoftLayer. Tutte le API sono sicure e codificate, cosicché i dati siano protetti.

Ad esempio, vuoi aggiungere capacità cognitive da Watson alle tue applicazioni in esecuzione su server bare metal da SoftLayer? Puoi aggiungere un servizio quale {{site.data.keyword.personalityinsightsshort}} per aiutare l'utente delle tue applicazioni in quattro passi:

1. Trova il servizio nel catalogo.
2. Fornisci un'istanza del servizio con pochi clic.
3. Imposta il servizio da eseguire con il codice esistente copiandone le credenziali e aggiungendole alla tua applicazione.
4. Effettuato l'aggiornamento nell'applicazione, distribuisci la nuova versione sulla tua infrastruttura SoftLayer.

Puoi ottenere una conoscenza di Insights and Cognitive richiamando le API Watson dalle tue applicazioni in SoftLayer per personalizzarle maggiormente. Oppure, utilizza i servizi Data and Analytics per accedere a un'analisi ad alte prestazioni per le tue applicazioni. In alternativa, selezionare un database-as-a-service in cui tu possa lasciare la gestione a {{site.data.keyword.Bluemix_notm}}.

Rinnova lo sviluppo delle tue applicazioni attraverso contenitori con servizi quali {{site.data.keyword.activedeployshort}} e {{site.data.keyword.deliverypipeline}}. Puoi quindi utilizzare il servizio {{site.data.keyword.vpn_short}} per comunicare con SoftLayer per connettere il tuo contenitore appartenente a una rete privata alla rete privata SoftLayer. Tutti gli addebiti di utilizzo dei servizi e delle risorse di calcolo sono riportati nella fattura {{site.data.keyword.Bluemix_notm}}.
