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

# Come calcolare i tuoi costi
{: #cost}

Puoi utilizzare differenti metodi per stimare il costo utilizzando le risorse PaaS (platform as a service) e IaaS (infrastructure as a service) {{site.data.keyword.Bluemix}} per creare e ospitare le tue applicazioni.
{:shortdesc}

Puoi utilizzare i seguenti metodi per determinare i tuoi costi:
* Utilizza il [pricing calculator ![Icona link esterno](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} per stimare il costo totale delle risorse dell'infrastruttura e della piattaforma che vuoi utilizzare.
* Utilizza gli stimatori del costo nella  {{site.data.keyword.pricing_sheet}} {{site.data.keyword.Bluemix_notm}}
per visualizzare una stima approssimativa del costo basata sulla dimensione della tua applicazione.
* Utilizza il calcolatore del costo nella pagina Prezzi per visualizzare i prezzi delle applicazioni accurati basati sul tuo input relativo agli utilizzi di runtime e servizi.
* Calcola il costo manualmente.

## Utilizzo del calcolatore dei prezzi
{: #pricing-calculator}

Puoi utilizzare il calcolatore dei prezzi per stimare il costo di molte risorse dell'infrastruttura e della piattaforma prima di fare un acquisto.
Il calcolatore dei prezzi fornisce le seguenti funzioni:
  * Le stime dei costi che al momento sono fornite in valuta USD.
  * Le stime delle risorse dell'infrastruttura che al momento sono disponibili per le categorie **Calcolo** e **Contenitori**.
  * Le stime dei costi delle risorse che al momento non includono sconti.
  * Le stime dei costi vengono fornite per scopi di pianificazione.

1. Accedi al calcolatore dei prezzi in uno dei seguenti modi:
  * Dalla pagina [Pricing ![Icona link esterno](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, fai clic su **Try the calculator** dalla sezione Explore our solutions.
  * Se non sei al momento collegato a {{site.data.keyword.Bluemix_notm}}, fai clic su **Prezzi** dalla homepage [{{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg)](https://console.bluemix.net/).
2. Dagli elenchi **Infrastruttura** o **Piattaforma**, seleziona la categoria della risorsa di cui vuoi il prezzo. Vengono visualizzate le risorse nella categoria selezionata e puoi anche ricercare la categoria per una risorsa specifica.
3. Selezionare una risorsa nella categoria per visualizzarne una descrizione. Alcune risorse hanno più opzioni. Ad esempio, se selezioni **Infrastruttura** > **Calcolo** > **Server bare metal**, puoi scegliere da un elenco di server.
4. Seleziona la quantità di risorse da aggiungere.
5. Fai clic su **Aggiungi per stimare**.
6. Continua ad aggiungere le risorse dalle categorie **Infrastruttura** e **Piattaforma** finché non hai aggiunto quello che vuoi stimare. Il pannello **Stima** mostra le risorse che hai aggiunto, il prezzo di ognuna e un prezzo totale.

Se stai stimando solo le risorse della piattaforma, per visualizzare una stima in una valuta diversa dai dollari statunitensi, puoi fare clic su **Ricerchi il calcolatore classico?**. Il calcolatore classico non include le risorse dell'infrastruttura.
{: tip}

### Utilizzo del calcolatore classico per le risorse della piattaforma
{: #calculator}

Per calcolare i costi delle risorse della piattaforma in una valuta diversa da USD, puoi utilizzare il calcolatore classico. Il calcolatore classico non fornisce le stime dei prezzi delle risorse dell'infrastruttura.

1. Vai al {{site.data.keyword.pricing_sheet}} {{site.data.keyword.Bluemix_notm}}.
2. Seleziona una delle opzioni nell'infrastruttura per supportare tutta la sezione dei carichi di lavoro.

Per utilizzare il calcolatore, digita il tuo utilizzo mensile previsto delle
risorse elencate, ad esempio il numero di istanze o le notifiche di push. Il calcolatore visualizza immediatamente il prezzo per il tuo
input. Puoi anche regolare il calcolatore per visualizzare i costi annuali invece dei costi mensili.

## Calcolo manuale dei tuoi costi
{: #manual}

Potresti voler stimare i tuoi costi di {{site.data.keyword.Bluemix_notm}} personalmente per comprendere meglio in che modo vengono calcolati i costi di {{site.data.keyword.Bluemix_notm}}. Puoi calcolare il prezzo totale
dell'utilizzo di {{site.data.keyword.Bluemix_notm}} per creare e ospitare la tua applicazione considerando i prezzi del runtime e i servizi che usa. I prezzi dei runtime e dei servizi a volte cambiano; pertanto, quando calcoli il prezzo totale, devi fare riferimento alle informazioni più recenti indicate nel listino dei prezzi {{site.data.keyword.Bluemix_notm}}.

## Valute di fatturazione supportate

La seguente tabella elenca le valute di fatturazione che sono disponibili.

|Codice ISO 4217| Valuta|
|-------------|---------|
|AUD |	  Dollaro australiano|
|BRL |	  Real brasiliano|
|CAD |	  Dollaro canadese|
|CHF |	  Franco svizzero|
|DKK |	  Corona danese|
|EUR |	  Euro|
|GBP |	  Sterlina britannica|
|INR |	  Rupia indiana|
|JPY |	  Yen giapponese|
|KRW |	  Won sudcoreano|
|NOK |	  Corona norvegese|
|NZD |	  Dollaro neozelandese|
|SEK |	  Corona svedese|
|USD |    Dollaro americano|
|ZAR |	  Rand sudafricano|
{:caption="Tabella 1. Valute supportate" caption-side="top"}

Se hai collegato i tuoi account {{site.data.keyword.Bluemix_notm}} e SoftLayer, ricevi un'unica fattura in dollari americani (USD). Per ulteriori informazioni, vedi [Fatturazione consolidata per gli account collegati](/docs/account/linking_accounts.html).
{: tip}
