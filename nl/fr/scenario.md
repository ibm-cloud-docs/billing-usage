---

copyright:

  years: 2015, 2018
lastupdated: "2017-10-09"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Scénario : Evaluation des coûts d'un exemple d'application Node
{: #sample}

Supposons que vous disposez d'une application Web Node.js avec capacité d'extensibilité et que l'application utilise plusieurs services fournis par {{site.data.keyword.Bluemix}}. Cet exemple explique comment le coût réel de votre application est calculé. L'application Web utilise les services et les éléments {{site.data.keyword.Bluemix_notm}} suivants :

* Quatre instances d'exécution Node.js de 256 Mo
* Deux stratégies {{site.data.keyword.autoscaling}}, un processeur et de la mémoire
* 2 Go par mois pour {{site.data.keyword.datacshort}}
* 150 Go par mois pour NoSQL Database, 100 000 appels API lourds et 500 000 appels API légers
* 20 Go pour le trafic réseau entrant et sortant

## Prix des ressources {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Pour que cet exemple reste simple, supposez que les prix figurant dans le tableau suivant ne fluctuent pas sur une période de
temps, par exemple sur un mois. La tarification dans cet exemple est en dollar.

|Service |	Fonctions |	Prix |
|--------|-----------|--------|
|SDK for Node.js |	375 Go/heure gratuits par mois (partagés entre tous les contextes d'exécution) |	0,07 $/Go/heure|
|{{site.data.keyword.autoscaling}} |	Plan de service gratuit pour le service {{site.data.keyword.autoscaling}} |	Gratuit|
|{{site.data.keyword.datacshort}} - Module de démarrage |	1 Go d'espace en cache et une réplique |	55,00 $/instance |
|{{site.data.keyword.datacshort}} -
Standard |	5 Go d'espace en cache et une réplique |	155,00 $/instance |
|{{site.data.keyword.datacshort}} -
Premium |	25 Go d'espace en cache et une réplique |	505,00 $/instance|
|IBM Cloudant® NoSQL DB for {{site.data.keyword.Bluemix_notm}} |	2 Go de stockage de données disponible<br/>50 000 appels API légers gratuits par mois<br/>10 000 appels API lourds gratuits par mois | $1.00 USD/GB<br/>$0.03 USD pour 1000 appels API légers<br/>$0.15 USD pour 1000 appels API lourds |
{:caption="Tableau 1. Tarification des ressources" caption-side="top"}

## Calcul du prix de l'application

Le prix de l'application peut être calculé comme suit :

<dl>
<dt>Quatre instances d'exécution Node.js de 256 Mo</dt>
<dd>{{site.data.keyword.Bluemix_notm}} facture un contexte d'exécution par Go/heure. Le nombre de Go utilisés par mois est <code>4 x 256 = 1024 Mo ou 1 Go par mois</code>. Supposez que vous utilisez <code>24 x 30
= 720 heures par mois</code> ; l'application est facturée <code>1 x 720 = 720 Go/heure</code>.
<p>
375 Go/heure sont inclus dans une franchise par mois et partagés entre tous les contextes d'exécution
{{site.data.keyword.Bluemix_notm}}. Par conséquent, le coût total du contexte d'exécution est <code>0,07 $ x
(720-375) = 24,15 $</code>.</p></dd>

<dt>Deux stratégies {{site.data.keyword.autoscaling}} (processeur et mémoire)</dt>
<dd>Les stratégies {{site.data.keyword.autoscaling}} sont gratuites.</dd>

<dt>2 Go par mois pour {{site.data.keyword.datacshort}}</dt>
<dd>Le plan de 50 Mo fourni par le service
{{site.data.keyword.datacshort}} est gratuit. Toutefois, il ne peut pas couvrir votre
utilisation
prévue de 2 Go par mois. Les trois plans payants pour {{site.data.keyword.datacshort}} coûtent une somme définie pour une quantité spécifique d'espace, quelle que soit la quantité d'espace que vous utilisez réellement. Par conséquent, il est judicieux de
choisir le plan le plus petit correspondant à l'utilisation que vous prévoyez, c'est-à-dire le plan standard de 5 Go. Le coût total est de 155 $ par mois.</dd>

<dt>150 Go par mois pour NoSQL Database</dt>
<dd>Le prix du service Cloudant NoSQL DB for {{site.data.keyword.Bluemix_notm}} dépend du stockage des données et de la possibilité d'accéder à ces données par différentes méthodes d'API. Les commandes <strong>PUT</strong> et
<strong>POST</strong> sont considérées comme des appels API lourds alors, que les commandes <strong>GET</strong> sont considérées comme des appels API
légers.
<p>
Additionnez le nombre de Go et déduisez une franchise gratuite de 2 Go. 148 Go sont facturés par
mois. Soustrayez la franchise gratuite de 50 000 appels API légers et de 10 000 appels API lourds. Le prix du stockage total inclut les éléments suivants :</p>
<pre class="codeblock">
<codeblock>
    148 x 1 = 148 $
    (450 000/1000) x 0,03 = 13,5 $
    (90 000/1000) x 0,15 = 13,5 $
</codeblock>
</pre>
<p>
Le prix total est de 148 + 13,5 + 13,5 = 175 $.</p></dd>

<dt>20 Go pour le trafic réseau entrant et sortant</dt>
<dd>Le trafic réseau entrant et sortant n'est pas facturé.</dd>

</dl>

Une fois tous les éléments ajoutés, le prix total de l'application est de 354,15 $.
