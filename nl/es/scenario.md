---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-30"

keywords: estimate cost, cost example, billing example, payment example, calculating app price

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Ejemplo: Estimación de costes de una app Node.js de ejemplo
{: #sample}

Suponga que tiene una app web de Node.js con prestaciones de escalabilidad y que la app utiliza varios servicios que suministra {{site.data.keyword.Bluemix}}. En este ejemplo, podrá aprender a calcular el coste real de la app. 
{: shortdesc}

La app web utiliza los servicios y elementos de {{site.data.keyword.Bluemix_notm}} siguientes:

* Cuatro instancias de tiempo de ejecución de 256 MB de Node.js
* Dos políticas, un procesador y una memoria de {{site.data.keyword.autoscaling}}
* 150 GB al mes de base de datos {{site.data.keyword.cloudant_short_notm}}, 1000 búsquedas, 500 escrituras y 50 consultas
* 20 GB de tráfico de red de entrada o de salida


## Precios para los recursos de {{site.data.keyword.Bluemix_notm}}
{: #sample_resources}

Para dar un ejemplo sencillo, suponga que los precios en la tabla siguiente no fluctúan en un intervalo de tiempo, por ejemplo, en un mes. En este ejemplo, todos los precios se indican en moneda de EE. UU.

| Servicio                           |	Características                                                            |	Precio             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	375 GB por hora gratuito al mes (compartido entre todos los tiempos de ejecución)            |	0,07 USD/GB por hora |
| {{site.data.keyword.autoscaling}} |	Plan de servicio gratuito para el servicio {{site.data.keyword.autoscaling}} |	Gratuito              |
| {{site.data.keyword.cloudant_short_notm}} | El plan Estándar incluye 20 GB de almacenamiento de datos gratuito</br>La capacidad de rendimiento suministrada escala en incrementos de:</br>100 búsquedas por segundo</br>50 escrituras por segundo</br>5 consultas por segundo | $1,00 USD/GB de almacenamiento de datos</br>$0,25 USD/Búsqueda por segundo</br>$0,50 USD/Escritura por segundo</br>$5,00 USD/Consulta por segundo |
{:caption="Tabla 1. Precios para los recursos" caption-side="top"}


## Cálculo del precio de una app
{: #calc-app-price}

El precio de la app se puede calcular de la forma siguiente:

<dl>
<dt>Cuatro instancias de tiempo de ejecución de 256 MB de Node.js</dt>
<dd>Cargos de {{site.data.keyword.Bluemix_notm}} para un tiempo de ejecución por GB por hora. El número de GB utilizados al mes es de <code>4 x 256 = 1024 MB o 1 GB al mes</code>. Suponga que hay <code>24 x 30 = 720 horas en un mes</code>, por consiguiente se le factura a la aplicación <code>1 x 720 = 720 GB por hora</code>.
<p>
375 GB por hora están incluidos en la concesión gratuita al mes, compartidos en todos los tiempos de ejecución de {{site.data.keyword.Bluemix_notm}}. Por consiguiente, el coste total para el tiempo de ejecución es de <code>0,07 dólares x (720-375) = 24,15 dólares</code>.</p></dd>

<dt>Dos políticas de {{site.data.keyword.autoscaling}} (procesador y memoria)</dt>
<dd>Las políticas de {{site.data.keyword.autoscaling}} son gratuitas.</dd>

<dt>150 GB al mes de {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>Los cargos del servicio {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} se basan en el almacenamiento de datos y en la posibilidad de acceder a dichos datos mediante la capacidad de rendimiento suministrada, representada en búsquedas, escrituras y consultas por segundo.
<p>
Añada el número de GB y deduzca los 20 GB de concesión gratuita. Se cargan 130 GB al mes. El precio de almacenamiento total incluye las partes siguientes:</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = 130$
    (1000 / 100) x 0,25 = 2,50$
    (500 / 50) x 0,50 = 5,00$
    (50 / 5) x 5,00 = 50,00$
</codeblock>
</pre>
<p>
El precio total es 130 + 2,50 + 5,00 + 50,00 = 187.50$.</p></dd>

<dt>20 GB de tráfico de red de entrada o de salida</dt>
<dd>El tráfico de red de entrada y salida está libre de cargo adicional.</dd>

</dl>

Cuando se añaden todos los elementos, el precio total de la aplicación es de 211,65 dólares.
