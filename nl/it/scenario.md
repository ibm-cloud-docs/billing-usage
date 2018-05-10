---

copyright:

  years: 2015, 2018
lastupdated: "2018-04-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Scenario: stima dei costi di un'applicazione nodo di esempio
{: #sample}

Supponi di avere un'applicazione web Node.js con funzionalità di ridimensionamento e che l'applicazione utilizzi diversi servizi forniti da {{site.data.keyword.Bluemix}}. Puoi capire in che modo viene calcolato il costo effettivo della tua applicazione nel seguente esempio. L'applicazione web utilizza i servizi e gli elementi di {{site.data.keyword.Bluemix_notm}} di seguito indicati:

* Quattro istanze di runtime Node.js di 256 MB
* Due politiche di {{site.data.keyword.autoscaling}}, processore e memoria
* 2 GB al mese di {{site.data.keyword.datacshort}}
* 150 GB al mese di database NoSQL, 100.000 chiamate API heavy e 500.000 chiamate API light.
* 20 GB di traffico di rete in entrata o in uscita

## Prezzi per le risorse {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Per non complicare l'esempio, presumi che i prezzi nella seguente
tabella non fluttuino entro un arco di tempo o tra archi di tempo diversi, ad esempio un mese. Tutti i prezzi in questo esempio
sono in dollari statunitensi.

|Servizio |	Funzioni |	Prezzo |
|--------|-----------|--------|
|SDK for Node.js |	375 GB-ore gratuiti al mese (condivise tra tutti i runtime) |	$0,07 USD/GB-ora|
|{{site.data.keyword.autoscaling}} |	Piano di servizio gratuito per il servizio {{site.data.keyword.autoscaling}} |	Gratuito|
|{{site.data.keyword.datacshort}} -
Starter |	1 GB di spazio di cache e una
                                replica |	$55,00 USD/istanza |
|{{site.data.keyword.datacshort}} -
Standard |	5 GB di spazio di cache e una
                                replica |	$155,00 USD/istanza |
|{{site.data.keyword.datacshort}} -
Premium |	25 GB di spazio di cache e una
                                replica |	$505,00 USD/istanza|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}} |	2 GB di archiviazione dati gratuita<br/>50.000 chiamate API light gratuite al mese<br/>10.000 chiamate API heavy gratuite al mese | $1,00 USD/GB<br/>$0,03 USD/1000 chiamate API light<br/>$0,15 USD/1000 chiamate API heavy |
{:caption="Tabella 1. Prezzi per le risorse" caption-side="top"}

## Calcolo del prezzo dell'applicazione

Il prezzo dell'applicazione può essere calcolato nel seguente modo:

<dl>
<dt>Quattro istanze di runtime Node.js di 256 MB</dt>
<dd>{{site.data.keyword.Bluemix_notm}} addebita un runtime in base ai GB-ore. Il numero di GB utilizzati al mese è <code>4 x 256 = 1024 MB o 1 GB al mese</code>. Presumi che ci siano <code>24 x 30 = 720 ore in un mese</code>; l'applicazione viene quindi addebitata per <code>1 x 720 = 720 GB-ore</code>.
<p>
375 GB-ore sono inclusi in una franchigia
al mese, condivisi tra tutti i runtime {{site.data.keyword.Bluemix_notm}}. Il costo totale per il runtime è pertanto <code>$0,07 x (720-375) = $24,15</code>.</p></dd>

<dt>Due politiche {{site.data.keyword.autoscaling}}
(processore e memoria)</dt>
<dd>Le politiche{{site.data.keyword.autoscaling}}
sono gratuite.</dd>

<dt>2 GB al mese di {{site.data.keyword.datacshort}}</dt>
<dd>Il piano da 50 MB
fornito dal servizio {{site.data.keyword.datacshort}} è
gratuito. Tuttavia, il piano libero non coprirebbe il tuo utilizzo previsto di 2 GB
al mese. I tre piani pagati per {{site.data.keyword.datacshort}} costano
un importo prefissato per una specifica quantità di spazio, indipendentemente da quanto spazio utilizzi. Pertanto, ti consigliamo di scegliere il piano minimo che soddisfa il tuo uso previsto, che è il
piano standard di 5 GB. Il costo totale è di $155 al mese.</dd>

<dt>150 GB al mese di database NoSQL</dt>
<dd>Gli addebiti del servizio Cloudant NoSQL DB {{site.data.keyword.Bluemix_notm}} sono basati sull'archiviazione di dati e sulla capacità di accedere a tali dati da parte di metodi API differenti. I comandi <strong>PUT</strong> e
<strong>POST</strong> sono considerati chiamate API heavy, ma i comandi <strong>GET</strong>
sono considerati chiamate API light.
<p>
Sommare il numero di GB e sottrarre
una franchigia di 2 GB. L'addebito mensile è di 148 GB. Sottrai la franchigia di 50.000 per le chiamate API light e di 10.000 per le chiamate API heavy. Il prezzo totale dell'archiviazione
include le seguenti parti:</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = $148
    (450.000 / 1000) x 0,03 = $13,5
    (90.000 / 1000) x 0,15 = $13,5
</codeblock>
</pre>
<p>
Il prezzo totale è 148 + 13,5 + 13,5 = $175.</p></dd>

<dt>20 GB di traffico di rete in entrata o in uscita</dt>
<dd>Il traffico di rete in entrata
e in uscita è gratuito.</dd>

</dl>

Una volta aggiunti tutti gli elementi, il prezzo totale dell'applicazione è di $354,15.
