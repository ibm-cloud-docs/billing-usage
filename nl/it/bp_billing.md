---

copyright:
  years: 2019
lastupdated: "2019-06-20"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Procedure consigliate per la fatturazione e l'utilizzo
{: #best-practices}

Segui le nostre procedure consigliate per tenere traccia dei costi e automatizzare la fatturazione in {{site.data.keyword.Bluemix}}.
{:shortdesc}


## Tieni traccia dei costi per le risorse correlate aggiungendo delle tag
{:#track-billing-tags}

Aggiungi le tag alle tue risorse per organizzare, tenere traccia e gestire i cosi per le risorse correlate. Quando utilizzi uno schema di contrassegno con tag coerente per identificare quali risorse sono correlate a progetti specifici, puoi raggruppare e filtrare tramite tali tag quando analizzi i costi all'interno del tuo report di utilizzo esportato.

1. Contrassegna con tag le risorse utilizzando uno schema di contrassegno con tag coerente, ad esempio creando delle tag per differenziare i centri di costi, i data center, i progetti o i team. Per aggiungere le tag, fai clic sull'icona Menu ![icona Menu](../icons/icon_hamburger.svg) > **Elenco risorse**. Nella colonna Tag, fai clic su **Aggiungi tag** per ogni risorsa che vuoi contrassegnare con tag.

   Aggiungi le tag in coppie chiave:valore per aggiungere delle colonne personalizzate basate sulla chiave nel report di utilizzo. Crea le chiavi in base alle categorie che utilizzi per organizzare le tue risorse, ad esempio utilizzando `costcenter:` per raggruppare per centro di costo o `project:` per raggruppare per progetto.
   {: tip}

   Ad esempio, potresti avere delle risorse per due progetti in un solo account, Project ABC e Project XYZ. Project ABC ha un cluster {{site.data.keyword.containershort_notm}}, alcune distribuzioni di applicazioni Cloud Foundry e un database {{site.data.keyword.cloudant_short_notm}}. Puoi aggiungere la tag `project:abc` a tutte queste risorse per distinguere quelle di Project ABC dalle risorse simili in Project XYZ che sono contrassegnate con `project:xyz`.

   Per ulteriori informazioni sull'aggiunta e l'utilizzo delle tag, vedi [Gestione delle tag](/docs/resources?topic=resources-tag).

1. Tieni traccia dei costi per le risorse contrassegnate con tag esportando il report di utilizzo per le tue istanze. Per esportare il report, vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Utilizzo**. Fai quindi clic su **Esporta CSV > Istanza**.

   Utilizza la colonna Tag nel file CSV dell'istanza per analizzare le risorse nel tuo account. Puoi ordinare i dati del CSV in base alla tag del progetto su ogni istanza in modo da poter analizzare meglio il costo dei singoli progetti. Se hai contrassegnato con tag le tue risorse con coppie chiave:valore, vedrai anche delle colonne nel report di utilizzo che corrispondono alla chiave. Ad esempio, le risorse contrassegnate con `project:abc` e `project:xyz` vengono visualizzate in una colonna Progetto come `abc` e `xyz`.

   Per ulteriori informazioni, vedi [Visualizzazione del tuo utilizzo](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automatizza la gestione di fatturazione e utilizzo tramite la CLI o le API
{: #billing-cli-apis}

Se vuoi automatizzare come controlli il tuo utilizzo di risorse e tutti i costi associati, puoi utilizzare la [CLI `ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) o le API [Misurazione utilizzo ![Icona link esterno](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} e [Report sull'utilizzo ![Icona link esterno](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} per integrare questa funzionalità nelle tue applicazioni.

Per iniziare ad utilizzare le API, configura [il dashboard di esempio di utilizzo {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}. Utilizzando {{site.data.keyword.openwhisk}}, l'esempio implementa un approccio controllato dall'API per ottenere e visualizzare i dati di fatturazione e utilizzo {{site.data.keyword.Bluemix_notm}}.
{: tip}
