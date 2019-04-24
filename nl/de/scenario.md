---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Szenario: Schätzen der Kosten für ein Beispiel-Knoten-App
{: #sample}

Angenommen, Sie haben eine Node.js-Web-App mit Skalierfunktionalität und die App nutzt verschiedene Services, die von {{site.data.keyword.Bluemix}} bereitgestellt werden. Dieses Beispiel zeigt, wie die tatsächlichen Kosten Ihrer App berechnet werden. Die Web-App nutzt die folgenden {{site.data.keyword.Bluemix_notm}}-Services und -Elemente:

* Vier 256-MB-Node.js-Laufzeitinstanzen
* Zwei {{site.data.keyword.autoscaling}}-Richtlinien (Prozessor und Speicher)
* 150 GB pro Monat für die {{site.data.keyword.cloudant_short_notm}}-Datenbank, 1000 Suchvorgänge, 500 Schreibvorgänge und 50 Abfragen.
* 20 GB Datenvolumen für ein- und ausgehenden Netzverkehr


## Preise für {{site.data.keyword.Bluemix_notm}}-Ressourcen
{: #sample_resources}

Nehmen Sie an, um das Beispiel einfach zu halten, dass die Preise in der folgenden Tabelle innerhalb eines Zeitrahmens oder zwischen zwei Perioden zum Beispiel eines Monats nicht schwanken. Alle Preisangaben in diesem Beispiel erfolgen in US-Währung.

| Service                           |	Features                                                            |	Preis             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	375 GB-Stunden pro Monat kostenfrei (für alle Laufzeiten gemeinsam)            |	$0,07 USD/GB-Stunde |
| {{site.data.keyword.autoscaling}} |	Kostenfreier Serviceplan für den {{site.data.keyword.autoscaling}}-Service |	Kostenfrei              |
| {{site.data.keyword.cloudant_short_notm}} für {{site.data.keyword.Bluemix_notm}} - Lite | 20 GB Datenspeicher kostenfrei</br>Skalierung der bereitgestellten Durchsatzkapazität in folgenden Schritten:</br>100 Suchvorgänge pro Sekunde</br>50 Schreibvorgänge pro Sekunde</br>5 Abfragen pro Sekunde | $ 1,00 USD/GB Datenspeicher</br>$ 0,25 USD/Suchvorgang pro Sekunde</br>$ 0,50 USD/Schreibvorgang pro Sekunde</br>$ 5,00 USD/Abfrage pro Sekunde |
{:caption="Tabelle 1. Preisstruktur für Ressourcen" caption-side="top"}


## Preis der App berechnen
{: #calc-app-price}

Der Preis der App kann auf die folgende Weise berechnet werden:

<dl>
<dt>Vier 256-MB-Node.js-Laufzeitinstanzen</dt>
<dd>{{site.data.keyword.Bluemix_notm}} rechnet für eine Laufzeit nach GB-Stunden ab. Die Anzahl der genutzten GB pro Monat beträgt <code>4 x 256 = 1024 MB oder 1 GB pro Monat</code>. Nehmen Sie an, dass <code>ein Monat 24 x 30 = 720 Stunden</code> hat, sodass für die Anwendung <code>1 x 720 = 720 GB-Stunden</code> berechnet werden.
<p>
375 GB-Stunden gehören zu den kostenfreien Leistungen eines Monats, die für alle {{site.data.keyword.Bluemix_notm}}-Laufzeiten genutzt werden können. Daher betragen die Gesamtkosten für die Laufzeit <code>$0,07 x (720-375) = $24,15</code>.</p></dd>

<dt>Zwei {{site.data.keyword.autoscaling}}-Richtlinien (Prozessor und Speicher)</dt>
<dd>Die {{site.data.keyword.autoscaling}}-Richtlinien sind gebührenfrei.</dd>

<dt>150 GB pro Monat für {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>Die Gebühren für den {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}}-Service basieren auf der Speicherung von Daten und auf der Möglichkeit, auf diese Daten anhand bereitgestellter Durchsatzkapazität zuzugreifen, die nach Suchvorgängen, Schreibvorgängen und Abfragen pro Sekunde definiert ist.
<p>
Addieren Sie die GB-Anzahl und ziehen Sie die kostenfreien 20 GB ab. 130 GB werden pro Monat in Rechnung gestellt. Der Gesamtspeicherpreis setzt sich dann wie folgt zusammen:</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $ 130
    (1000 / 100) x 0,25 = $ 2,50
    (500 / 50) x 0,50 = $ 5,00
    (50 / 5) x 5,00 = $ 50,00
</codeblock>
</pre>
<p>
Gesamtpreis: 130 + 2,50 + 5,00 + 50,00 = $ 187,50.</p></dd>

<dt>20 GB Datenvolumen für ein- und ausgehenden Netzverkehr</dt>
<dd>Eingehender und ausgehender Netzdatenverkehr ist gebührenfrei.</dd>

</dl>

Wenn alle Positionen addiert werden, beträgt der Gesamtpreis der Anwendung $ 211,65.
