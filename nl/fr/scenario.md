---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-15"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Scénario : Evaluation des coûts d'un exemple d'application Node
{: #sample}

Supposons que vous disposez d'une application Web Node.js ayant des capacités d'extensibilité et que l'application utilise plusieurs services fournis par {{site.data.keyword.Bluemix}}. Cet exemple explique comment le coût réel de votre application est calculé. L'application Web utilise les services et les éléments {{site.data.keyword.Bluemix_notm}} suivants :

* Quatre instances d'exécution Node.js de 256 Mo
* Deux stratégies {{site.data.keyword.autoscaling}}, un processeur et de la mémoire
* Base de données {{site.data.keyword.cloudant_short_notm}} de 150 Go par mois, 1 000 recherches, 500 écritures et 50 requêtes. 
* 20 Go pour le trafic réseau entrant et sortant


## Prix des ressources {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Pour que cet exemple reste simple, nous supposerons que les prix figurant dans le tableau suivant ne fluctuent pas sur une période de
temps, par exemple sur un mois. La tarification dans cet exemple est en dollar.

|Service |	Fonctions |	Prix |
|--------|-----------|--------|
|SDK for Node.js |	375 Go/heure gratuits par mois (partagés entre tous les contextes d'exécution) |	0,07 $/Go/heure|
|{{site.data.keyword.autoscaling}} |	Plan de service gratuit pour le service {{site.data.keyword.autoscaling}} |	Gratuit|
|{{site.data.keyword.cloudant_short_notm}} pour {{site.data.keyword.Bluemix_notm}} - Lite| Inclut 20 Go de stockage de données disponible</br>Evolutivité de la capacité de débit mise à disposition par incréments de :</br>100 recherches par seconde</br>50 écritures par seconde</br>5 requêtes par seconde | 1,00 $ USD/Go de stockage de données</br>0,25 $ USD/recherche par seconde</br>0,50 $ USD/écriture par seconde</br>5,00 $ USD/requête par seconde |
{:caption="Tableau 1. Tarification des ressources" caption-side="top"}


## Calcul du prix de l'application
{: #calc-app-price}

Le prix de l'application peut être calculé comme suit :

<dl>
<dt>Quatre instances d'exécution Node.js de 256 Mo</dt>
<dd>{{site.data.keyword.Bluemix_notm}} facture un contexte d'exécution par Go/heure. Le nombre de Go utilisés par mois est <code>4 x 256 = 1024 Mo ou 1 Go par mois</code>. Supposez que vous utilisez <code>24 x 30
= 720 heures par mois</code> ; l'application est facturée <code>1 x 720 = 720 Go/heure</code>.
<p>
375 Go/heure sont inclus dans une franchise par mois qui est partagée entre tous les contextes d'exécution
{{site.data.keyword.Bluemix_notm}}. Par conséquent, le coût total du contexte d'exécution est <code>0,07 $ x
(720-375) = 24,15 $</code>.</p></dd>

<dt>Deux stratégies {{site.data.keyword.autoscaling}} (processeur et mémoire)</dt>
<dd>Les stratégies {{site.data.keyword.autoscaling}} sont gratuites.</dd>

<dt>150 Go par mois pour {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>Le service {{site.data.keyword.cloudant_short_notm}} pour {{site.data.keyword.Bluemix_notm}} dépend du stockage des données et de la possibilité d'accéder à ces données par la capacité de débit mise à disposition définie par les recherches, les écritures et les requêtes par seconde. 
<p>
Additionnez le nombre de Go et déduisez la franchise gratuite de 20 Go. 130 Go sont facturés par mois. Le prix du stockage total inclut les éléments suivants :</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = 130 $
    (1 000 / 100) x 0,25 = 2,50 $
    (500 / 50) x 0,50 = 5,00 $
    (50 / 5) x 5,00 = 50,00 $
</codeblock>
</pre>
<p>
Le prix total est 130 + 2,50 + 5,00 + 50,00 = 187,50 $.</p></dd>

<dt>20 Go pour le trafic réseau entrant et sortant</dt>
<dd>Le trafic réseau entrant et sortant n'est pas facturé.</dd>

</dl>

Une fois tous les éléments ajoutés, le prix total de l'application est de 211,65 $.
