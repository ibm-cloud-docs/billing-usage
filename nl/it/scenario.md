---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-15"

keywords: estimate cost, cost example, billing example, payment example

subcollection: billing-usage

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
* 150 GB al mese di database {{site.data.keyword.cloudant_short_notm}}, 1.000 ricerche, 500 scritture e 50 query.
* 20 GB di traffico di rete in entrata o in uscita


## Prezzi per le risorse {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Per non complicare l'esempio, presumi che i prezzi nella seguente
tabella non fluttuino entro un arco di tempo o tra archi di tempo diversi, ad esempio un mese. Tutti i prezzi in questo esempio
sono in dollari statunitensi.

| Servizio                           |	Funzioni                                                            |	Prezzo             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	375 GB-ore gratuiti al mese (condivise tra tutti i runtime)            |	$0,07 USD/GB-ora |
| {{site.data.keyword.autoscaling}} |	Piano di servizio gratuito per il servizio {{site.data.keyword.autoscaling}} |	Gratuito              |
| {{site.data.keyword.cloudant_short_notm}} per {{site.data.keyword.Bluemix_notm}} - Lite | Include 20 GB di archiviazione dati gratuita</br>Ridimensiona la capacità produttiva fornita con incrementi di:</br>100 ricerche al secondo</br>50 scritture al secondo</br>5 query al secondo | $1,00 USD/GB di archiviazione dati</br>$0,25 USD/Ricerca al secondo</br>$0,50 USD/Scrittura al secondo</br>$5,00 USD/Query al secondo |
{:caption="Tabella 1. Prezzi per le risorse" caption-side="top"}


## Calcolo del prezzo dell'applicazione
{: #calc-app-price}

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

<dt>150 GB al mese di {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>Gli addebiti del servizio {{site.data.keyword.cloudant_short_notm}} per {{site.data.keyword.Bluemix_notm}} si basano sull'archiviazione dei dati e sulla capacità di accedere a tali dati mediante la capacità produttiva fornita denotata da ricerche, scritture e query al secondo.
<p>
Somma il numero di GB e sottrai la franchigia di 20 GB. L'addebito mensile è di 130 GB. Il prezzo totale dell'archiviazione
include le seguenti parti:</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1.000 / 100) x 0,25 = $2,50
    (500 / 50) x 0,50 = $5
    (50 / 5) x 5,00 = $50
</codeblock>
</pre>
<p>
Il prezzo totale è 130 + 2,50 + 5 + 50 = $187,50.</p></dd>

<dt>20 GB di traffico di rete in entrata o in uscita</dt>
<dd>Il traffico di rete in entrata
e in uscita è gratuito.</dd>

</dl>

Una volta aggiunti tutti gli elementi, il prezzo totale dell'applicazione è di $211,65.
