---

copyright:

  years: 2015, 2018

lastupdated: "2018-06-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Cómo calcular sus costes
{: #cost}

Puede utilizar distintos métodos para estimar el coste de utilizar los recursos de plataforma como servicio (PaaS) e infraestructura como servicio (IaaS) de {{site.data.keyword.Bluemix}} para crear y alojar sus apps.
{:shortdesc}

Puede utilizar los métodos siguientes para determinar los costes:
* Utilice la [calculadora de precios![Icono de enlace externo](../icons/launch-glyph.svg)](https://console.bluemix.net/pricing/){: new_window} para estimar el coste total de los recursos de plataforma e infraestructura que desea utilizar.
* Utilice los estimadores de costes de la {{site.data.keyword.pricing_sheet}} de {{site.data.keyword.Bluemix_notm}} para ver una estimación aproximada del coste en función del tamaño de la app.
* Utilice la calculadora de costes de la página Precios para ver precios precisos de la app en función de la entrada del tiempo de ejecución y del uso de los servicios.
* Calcule el coste manualmente.

## Uso de la calculadora de precios
{: #pricing-calculator}

Puede utilizar la calculadora de precios para estimar el coste de los recursos de plataforma e infraestructura antes de realizar una compra.
La calculadora de precios proporciona las siguientes funciones:
  * Estimaciones de costes que se proporcionan en USD.
  * Estimaciones para recursos de infraestructura que están disponibles en las categorías **Cálculo** y **Contenedores**.
  * Estimaciones de coste de recursos que actualmente no incluyen descuentos.
  * Estimaciones de costes para fines de planificación.

1. Acceda a la calculadora de precios en una de las siguientes formas:
  * Desde la [página Tarifas![Icono de enlace externo](../icons/launch-glyph.svg)](https://www.ibm.com/cloud/pricing){: new_window}, pulse **Probar la calculadora** desde la sección Explorar nuestras soluciones.
  * Si no ha iniciado sesión en {{site.data.keyword.Bluemix_notm}}, pulse **Tarifas** desde la [ página de inicio de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg)](https://console.bluemix.net/).
2. En las listas **Infraestructura** o **Plataforma**, seleccione la categoría del recurso para el que desea establecer un precio. Se muestran los recursos de la categoría que ha seleccionado, y también puede buscar la categoría de un recurso específico.
3. Seleccione un recurso de la categoría para ver una descripción del mismo. Algunos recursos tienen varias opciones. Por ejemplo, si selecciona **Infraestructura** > **Calcular** > **Servidores nativos**, podrá elegir de una lista de servidores.
4. Seleccione la cantidad del recurso que desea añadir.
5. Pulse **Añadir a la estimación**.
6. Continúe añadiendo recursos de las categorías **Infraestructura** y **Plataforma** hasta que añada lo que desee estimar. El panel **Estimación** muestra los recursos que ha añadido, el precio de cada uno y un precio total.
7. Opcionalmente, para crear un PDF de la información del panel **Estimación** cuando haya terminado de compilar la lista de recursos, pulse **Descargar PDF**. Puede que desee crear un PDF, por ejemplo, para revisar los recursos de los que está estableciendo el precio antes de comprar o para utilizar como una guía al adquirir los recursos.


Si solo está estableciendo el precio de los recursos de plataforma, puede pulsar **¿Está buscando una calculadora clásica?** para ver una estimación en una moneda que no sea USD. La calculadora clásica no incluye recursos de infraestructura.
{: tip}

### Uso de la calculadora clásica para recursos de plataforma
{: #calculator}

Para calcular los costes del recurso de plataforma en una moneda que no sea USD, puede utilizar la calculadora clásica. La calculadora clásica no proporciona estimaciones de precio para recursos de infraestructura.

1. Vaya a la {{site.data.keyword.pricing_sheet}} de {{site.data.keyword.Bluemix_notm}}.
2. Seleccione una de las opciones de la sección Infraestructura para dar soporte a todas las cargas de trabajo.

Para utilizar la calculadora, escriba el uso mensual proyectado de los recursos listados; por ejemplo, el número de instancias o notificaciones por push. La calculadora muestra inmediatamente el precio de la entrada. También puede ajustar la calculadora para que muestre costes anuales en lugar de costes mensuales.

## Cálculo manual de los costes
{: #manual}

Es posible que desee calcular los costes {{site.data.keyword.Bluemix_notm}} usted mismo para entender mejor cómo se calculan los costes en {{site.data.keyword.Bluemix_notm}}. Puede calcular el precio total derivado de utilizar {{site.data.keyword.Bluemix_notm}} para crear y alojar su app teniendo en cuenta los precios de tiempo de ejecución y los servicios que utiliza. Los precios de los tiempos de ejecución y de los servicios pueden cambiar a veces; por consiguiente, debe hacer referencia a la información más reciente en el precio de hoja de precios de {{site.data.keyword.Bluemix_notm}} a la hora de calcular el precio de la hoja total.

## Monedas de facturación soportadas

La tabla siguiente lista las monedas de facturación disponibles.

|Código ISO 4217| Moneda|
|-------------|---------|
|AUD |	  Dólar australiano|
|BRL |	  Real brasileño|
|CAD |	  Dólar canadiense|
|CHF |	  Franco suizo|
|DKK |	  Corona danesa|
|EUR |	  Euro|
|GBP |	  Libra esterlina|
|INR |	  Rupia india|
|JPY |	  Yen japonés|
|KRW |	  Won de Corea del Sur|
|NOK |	  Corona noruega|
|NZD |	  Dólar neozelandés|
|SEK |	  Corona sueca|
|USD |    Dólar estadounidense|
|ZAR |	  Rand sudafricano|
{:caption="Tabla 1. Monedas soportadas" caption-side="top"}

Si ha enlazado las cuentas de {{site.data.keyword.Bluemix_notm}} y SoftLayer, la única factura que recibirá estará solo en dólares de Estados Unidos (USD). Para obtener más información, consulte [Facturación consolidada para cuentas enlazadas](/docs/account/linking_accounts.html).
{: tip}
