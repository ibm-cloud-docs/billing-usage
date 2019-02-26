---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Visualizzazione del tuo utilizzo
{: #viewingusage}

Puoi visualizzare i tuoi dettagli di utilizzo, compreso un riepilogo degli addebiti stimati per tutte le risorse e tutti i servizi e i piani di supporto utilizzati ogni mese nelle tue organizzazioni, dalla pagina Utilizzo nella console {{site.data.keyword.Bluemix}}.
{:shortdesc}

I gestori fatturazione possono visualizzare i dettagli solo per le organizzazioni in cui è ad essi assegnato il ruolo di Gestore fatturazione.
{: note}


## Visualizzazione delle autorizzazioni di utilizzo
{: #view-usage-permissions}

Per le risorse gestite da Cloud Foundry, il ruolo di Gestore fatturazione deve essere applicato al livello dell'organizzazione. Per visualizzare l'utilizzo delle risorse {{site.data.keyword.Bluemix}} IAM (Identity and Access Management), al gruppo di risorse deve essere applicato il ruolo Visualizzatore. Per ulteriori informazioni sui ruoli di autorizzazione, vedi [Accesso IAM](/docs/iam?topic=iam-userroles), [Accesso Cloud Foundry](/docs/iam?topic=iam-cfaccess) o [Autorizzazioni dell'infrastruttura classica](/docs/iam?topic=iam-infrapermission).

## Visualizzazione dei dettagli di utilizzo dei servizi
{: #services}

Nella sezione dei servizi, puoi visualizzare un elenco dei tuoi servizi e i costi stimati a essi associati. Per visualizzare un riepilogo degli addebiti stimati per tutte le istanze di una specifica risorsa, completa la seguente procedura:

1. Vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Utilizzo**.
2. Fai clic su **Visualizza istanze** per visualizzare tutte le istanze di uno specifico tipo di risorsa.  
3. Per visualizzare un riepilogo dettagliato degli addebiti stimati per ciascuna istanza di uno specifico tipo di risorsa, fai clic su **Visualizza i dettagli dell'istanza**. Puoi anche visualizzare le metriche dettagliate dell'utilizzo mensile per l'istanza selezionata.

Al proprietario dell'account viene addebitato l'utilizzo totale sostenuto su tutte le organizzazioni alla fine di ciascun ciclo di fatturazione. Ogni ciclo di fatturazione dura un mese.

I proprietari dell'account possono filtrare il riepilogo di utilizzo in base al gruppo e selezionare il periodo di tempo per l'utilizzo. Gli addebiti visualizzati rappresentano l'importo che ti viene addebitato per quel mese in qualità di proprietario dell'account.

Se selezioni una specifica organizzazione dall'elenco **Filtra per gruppo**, puoi vedere l'utilizzo totale per tale organizzazione, compresi gli eventuali utilizzi come parte di un livello gratuito. L'utilizzo del periodo di prova gratuito viene visualizzato come gratuito, a livello dell'account, ma non a livello dell'organizzazione. Quando visualizzi l'utilizzo dell'organizzazione, vedi l'utilizzo reale per tale organizzazione, che include sia l'utilizzo a titolo gratuito che quello che viene invece addebitato. Tutto l'utilizzo dell'organizzazione viene sommato all'utilizzo dell'account dopo la rimozione del periodo di prova gratuito.

Il gestore dell'account di un account Pagamento a consumo, può impostare le notifiche di spesa rispetto al costo totale dell'account, per il
runtime, i servizi e per i singoli servizi, esclusi quelli di terze parti. Per ulteriori informazioni, vedi [Impostazione delle notifiche di spesa](/docs/billing-usage?topic=billing-usage-spending).

## Esportazione dei dettagli di utilizzo in un file `.csv`
{: #export-csv}

Puoi esportare un riepilogo del tuo utilizzo, o informazioni sui tuoi servizi e le tue istanze, in un file CSV. Esportando il tuo file CSV, puoi facilmente trovare le informazioni sulle stime dei costi e sull'utilizzo per ciascuna risorsa per gli storni degli addebiti ai tuoi clienti o per saperne di più sui tuoi costi.

1. Vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Utilizzo**.
2. Fai clic su **Esporta CSV**.  
