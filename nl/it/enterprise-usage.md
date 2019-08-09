---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Visualizzazione dell'utilizzo in un'azienda
{: #enterprise-usage}

Puoi tenere traccia dei costi di risorse e supporto dagli account nella tua azienda {{site.data.keyword.Bluemix}} visualizzandone l'utilizzo. Gli account e i gruppi di account di cui puoi visualizzare l'utilizzo dipendono dal tuo accesso assegnato.
{: shortdesc}

Le aziende {{site.data.keyword.Bluemix_notm}} ti consentono di gestire in modo centralizzato più account {{site.data.keyword.Bluemix_notm}}. Come utente aziendale, puoi controllare l'utilizzo delle risorse e i costi associati per tutti gli account nell'azienda. Vedi [Cos'è un'azienda?](/docs/account?topic=account-enterprise) per ulteriori informazioni.

## Accesso richiesto per la visualizzazione dell'utilizzo aziendale.
{: #enterprise-usage-access}

In un'azienda, l'accesso alle informazioni sull'utilizzo viene controllato dal servizio aziendale. Per visualizzare le informazioni sull'utilizzo, gli utenti devono essere invitati nell'account aziendale e avere il ruolo di amministratore, editor o visualizzatore dei report di utilizzo sul servizio aziendale. Il ruolo di visualizzatore dei report di utilizzo fornisce l'accesso solo per visualizzare i report di utilizzo, mentre i ruoli di editor e amministratore consentono ulteriori azioni di gestione dell'azienda. In linea con le procedure consigliate sulla sicurezza, assegna la minor quantità di accesso necessaria all'utente per completare le proprie attività. Per ulteriori informazioni, vedi [Azioni e ruoli dell'azienda](/docs/iam?topic=iam-account-services#enterprise-account-management).

Puoi fornire agli utenti accesso granulare in modo che possono visualizzare l'utilizzo di un particolare account o gruppo di account. Ad esempio, diciamo che la tua azienda ha dei gruppi di account per ogni dipartimento e ogni dipartimento ha dei gruppi di accesso per ogni team. Puoi destinare l'accesso in modo che ogni utente dell'azienda possa visualizzare solo le informazioni necessarie per svolgere il proprio ruolo lavorativo.
   * Il tuo direttore finanziario deve visualizzare l'utilizzo per l'intera azienda in modo che possa tenere traccia e recuperare i costi di ogni dipartimento, ma non ha bisogno di creare degli account o gruppi di account. Assegnagli il ruolo di visualizzatore dei report di utilizzo per l'azienda.
   * Ciascun responsabile di dipartimento deve visualizzare l'utilizzo del proprio dipartimento e anche creare e gestire gli account e i gruppi di account dei propri team. Assegna a ciascun responsabile di dipartimento il ruolo di editor per il gruppo di account del proprio dipartimento.
   * Ciascun responsabile del team deve visualizzare l'utilizzo del proprio team, ma vuoi che ottenga l'approvazione del dipartimento per aggiungere nuovi account al proprio team. Assegna ad ogni responsabile del team il ruolo di visualizzatore dei report di utilizzo per il gruppo di account del proprio team. Può visualizzare l'utilizzo da tutti gli account all'interno del gruppo di account, ma non quello dai gruppi di account di altri team nel dipartimento.

Per la procedura dettagliata sull'assegnazione dell'accesso aziendale, vedi [Assegnazione dell'accesso aziendale](/docs/iam?topic=iam-assign-access-enterprise).

## Visualizzazione dell'utilizzo dell'azienda
{: #enterprise-usage-console}

1. Accedi all'account dell'azienda.
1. Vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Utilizzo**.

   La pagina Utilizzo visualizza i costi di tutto l'utilizzo delle risorse nella tua azienda, suddiviso per account e gruppo di account. Puoi anche visualizzare l'utilizzo dei crediti di supporto per l'intera azienda e tutti i costi che si sono verificati.

   Le informazioni di utilizzo per i servizi dell'infrastruttura classica non sono incluse nel periodo di fatturazione corrente. Tuttavia, sono incluse per i precedenti periodi di fatturazione, che puoi visualizzare selezionando un mese precedente dal menu **Intervallo di tempo**. Per ulteriori informazioni, vedi [Visualizzazione dell'utilizzo per le tue risorse dell'infrastruttura classica](/docs/billing-usage?topic=billing-usage-infra-usage).
1. Per visualizzare l'utilizzo all'interno di un gruppo di account, fai clic sul nome del gruppo di account nella tabella o sul menu **Livello aziendale**. In modo simile al livello aziendale, l'utilizzo viene suddiviso per account e gruppo di account.

   Se un gruppo di account non contiene alcun account, non viene visualizzato nella pagina Utilizzo.

1. Per visualizzare l'utilizzo per risorsa, vai al livello dell'account facendo clic sui gruppi di account nella tabella o selezionando l'account dal menu **Livello aziendale**. I costi vengono visualizzati per ogni tipo di risorsa utilizzata durante il periodo di tempo.

   Dall'account aziendale, non puoi visualizzare i dati di utilizzo per il piano o l'istanza della risorsa perché questo richiede l'accesso all'account. Se sei un utente nell'account, passa all'account per visualizzare questi dati. Hai bisogno dell'accesso di fatturazione alle risorse e ai servizi nell'account come descritto in [Visualizzazione del tuo utilizzo](/docs/billing-usage?topic=billing-usage-viewingusage).

Vengono visualizzati solo i dati per l'utilizzo che si verifica per gli account nell'azienda nell'account aziendale. Per visualizzare l'utilizzo prima dell'aggiunta di un account all'azienda, accedi a tale account e seleziona il periodo di tempo pertinente.
{: note}

### Visualizzazione dell'utilizzo aziendale utilizzando la CLI
{: #enterprise-usage-cli}

Puoi ottenere un report di utilizzo per l'azienda, un gruppo di account o un account specifico.

1. Accedi e seleziona l'account aziendale.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. Se vuoi visualizzare l'utilizzo per uno specifico gruppo di account o account, trova il nome o l'ID eseguendo il comando **`ibmcloud enterprise`**.

   Ad esempio, il seguente comando visualizza tutti i gruppi di account in un'azienda.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. Visualizza l'utilizzo eseguendo il comando **`ibmcloud billing`** come mostrato nei seguenti esempi:

   * Visualizza l'utilizzo per l'intera azienda per il mese corrente.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * Visualizza l'utilizzo per il gruppo di account `Development` per luglio 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * Visualizza l'utilizzo per i gruppi di account e gli account che si trovano al livello direttamente sotto l'azienda.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   Per impostazione predefinita, i comandi generano il report di utilizzo per il mese corrente nel seguente formato. La maggior parte dei costi vengono elencati come costi fatturabili. I costi non fatturabili vengono elencati solo in casi molto rari, ad esempio per il mese in cui aggiungi un account di prova all'azienda.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   Puoi generare il report in formato JSON specificando l'opzione `--output JSON`.
   {: tip}

### Visualizzazione dell'utilizzo aziendale utilizzando l'API
{: #enterprise-usage-api}

Puoi ottenere i report di utilizzo da un'azienda e i propri account richiamando l'<!-- [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external} -->API Enterprise Usage Reports (Beta). Puoi basare la query nella tua chiamata API su un'azienda, un gruppo di account o un account e specificare se visualizzare l'entità o i suoi elementi secondari. L'API Enterprise Usage Reports è una release beta.

I seguenti esempi mostrano le query che puoi utilizzare per ottenere report di utilizzo diversi. Quando richiami l'API, sostituisci le variabili ID e il token IAM con i valori dalla tua azienda. 

Visualizza l'utilizzo per l'intera azienda per il mese corrente.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Visualizza l'utilizzo per un gruppo di account per il mese di luglio 2019.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Visualizza l'utilizzo per i gruppi di account e gli account che si trovano al livello direttamente sotto l'azienda.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Recupero dei costi per l'utilizzo aziendale
{: #enterprise-cost-recovery}

Un'azienda consolida la fatturazione da tutti i propri account e gruppi di account su una singola fattura, che semplifica la gestione della fatturazione. Puoi recuperare i costi dall'utilizzo delle risorse nell'azienda addebitando i costi di utilizzo di ogni gruppo di account o account al team o dipartimento associato.

Per visualizzare la tua gerarchia aziendale e tutto l'utilizzo, hai bisogno di una politica di accesso con il ruolo di editor o amministratore sul servizio aziendale per l'intera azienda. La seguente procedura utilizza la console {{site.data.keyword.Bluemix_notm}} come esempio, ma puoi anche eseguirla tramite la CLI o l'API.

1. Trova i costi di utilizzo per ogni dipartimento andando a **Gestisci > Utilizzo** nell'account aziendale. Dal menu **Intervallo di tempo**, seleziona il mese precedente per visualizzare l'utilizzo incluso nell'ultima fattura.

  I costi per i tuoi gruppi di account vengono elencati nella tabella. Questi costi sono tutti addebitati con l'eccezione di tutte le tasse addebitate nella tua regione di fatturazione. Se vuoi un'ulteriore suddivisione dei costi di utilizzo, fai clic sul nome del gruppo di account per visualizzare gli account e i gruppi di account che contiene.

1. Identifica i dipartimenti all'interno della tua società che corrispondono ai gruppi di account.

   Se i contatti assegnati ai tuoi gruppi di account sono associati al dipartimento da cui vuoi recuperare i costi, trovare il contatto è uno dei modi per trovare queste informazioni. Vai a **Gestisci > Azienda** e seleziona **Account**. Il contatto di ogni gruppo di account viene elencato nella tabella.

   Tuttavia, le procedure di fatturazione variano in base alla società. Ad esempio, il contatto del gruppo di account potrebbe essere un punto focale tecnico non associato al dipartimento che vuoi far pagare. Verifica sempre il dipartimento corretto in base ai processi di contabilità della tua società.

   Se la tua società utilizza dei codici di fatturazione per addebitare i costi ai dipartimenti, aggiungi il codice di fatturazione al nome del gruppo di account per identificare facilmente il codice. Ad esempio, `Sales - A2B3`.
   {: tip}

1. Accoppia i costi di utilizzo di ogni gruppo di account con il dipartimento identificato e segui i processi della tua società per inviare gli addebiti.
