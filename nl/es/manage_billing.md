---



copyright:

  years: 2017, 2018
lastupdated: "2017-12-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Gestión de la utilización de cuentas enlazadas de {{site.data.keyword.Bluemix_notm}}
{: #linkedusage}

Si ha enlazado una cuenta de {{site.data.keyword.Bluemix}} y otra de SoftLayer, utilice el portal del cliente para realizar pagos puntuales, cambiar los detalles de su tarjeta de pago, ver los artículos facturados y sus facturas.
{: shortdesc}

Las opciones de facturación y utilización que se visualizan en la consola de {{site.data.keyword.Bluemix_notm}} pueden diferir según si tiene una cuenta gratuita o si no tiene las cuentas de {{site.data.keyword.Bluemix_notm}} y SoftLayer enlazadas.
{: tip}

## Efectuar un pago
{: #makepayment}

Puede realizar un pago puntual siempre que lo desee. El pago puede ser por la totalidad del saldo o un importe parcial. Los detalles que especifique para el pago no se registran. Siga los siguientes pasos para realizar un pago único.

1. Seleccione una de las opciones siguientes dependiendo del panel de control que esté utilizando:   
 * Desde el panel de control de Apps o Servicios, pulse **Gestionar** > **Facturación y utilización** > **Realizar un pago**.  
 * Desde el panel de control de Infraestructura, pulse **Cuenta** > **Hacer un pago**.
3. En el campo **Importe del pago**, especifique la cantidad que desea pagar.
4. Seleccione un método de pago:
 * Pago con una tarjeta de crédito. Especifique los detalles y la dirección de facturación de la tarjeta. A continuación, pulse **Realizar pago con tarjeta de crédito**.
 * Pago con PayPal. Especifique sus detalles cuando le sean solicitados para poder completar el pago.

Resuelva cualquier problema que se le pueda presentar al efectuar el pago. El Saldo de la cuenta se actualizará una vez que se haya aceptado el pago. Puede ponerse en contacto con el equipo de soporte pulsando **Soporte** > **Añadir incidencia**.

## Cambiar su método de pago
{: #changepaymethod}

Cada cuenta facturable debe tener una tarjeta de crédito registrada que sea válida. Cada mes, se cargará en la tarjeta de crédito la cantidad utilizada que se acumule durante dicho mes. En la consola de {{site.data.keyword.Bluemix_notm}}, complete los siguientes pasos para cambiar sus detalles de pago.

1. Seleccione una de las opciones siguientes dependiendo del panel de control que esté utilizando:  
 * Desde el panel de control de Apps o Servicios, pulse **Gestionar** > **Facturación y utilización** > **Modificar método de pago**.  
 * Desde el panel de control de Infraestructura, pulse **Cuenta** > **Facturación** > **Método de pago**.
2. En la sección Añadir método de pago, especifique los detalles y la dirección de facturación de la tarjeta de crédito. A continuación, pulse **Añadir tarjeta de crédito**.

Se validarán los detalles de la tarjeta y, a continuación, estará disponible para utilizarse en su cuenta en 24 horas. Se enviará un correo electrónico de confirmación al contacto especificado en la sección de la dirección de facturación de la tarjeta.

## Visualizar los artículos facturados
{: #viewbilling}

Puede asociar los artículos a facturar a dispositivos específicos, y también puede eliminar la asociación a los mismos. De forma predeterminada, la página de Artículos de facturación visualiza los artículos de facturación asociados. La vista se puede cambiar seleccionando una opción desde el menú de visualización. La asociación y la eliminación de la asociación se puede realizar para un artículo, o para más de un artículo a la vez utilizando la operación de Acciones masivas. Los artículos de facturación individuales se pueden cancelar siempre que lo desee desde la página Artículos de facturación. Complete los siguientes pasos para asociar o eliminar la asociación de los elementos de facturación en la consola.

1. Seleccione una de las opciones siguientes dependiendo del panel de control que esté utilizando:   
 * Desde el panel de control de Apps o Servicios, pulse **Gestionar** > **Facturación y utilización** > **Facturación**.  
 * Desde el panel de control de Infraestructura, pulse **Cuenta** > **Facturación** > **Artículos de facturación**.
2. Para filtrar la vista, seleccione una opción de elemento de facturación de la lista.

## Visualizar facturas
{: #viewinvoices}

Las facturas pueden verse o pagarse en cualquier momento. Cada factura viene resumida con su Número de factura, Fecha, Tipo de factura así como con otros saldos monetarios. Los tipos de factura se clasifican de la siguiente manera:

 *  Nueva: la primera factura de una serie recurrente de facturas
 *  Recurrente: una factura de cargos recurrente que han estado activos en la cuenta por más de un mes
 *  Cargo puntual: un cargo puntual de distintos gastos, que pueden incluir los sobrecostes
 *  Cargo: un cargo de {{site.data.keyword.Bluemix_notm}} en el saldo de su cuenta
 *  Devolución: una devolución o desembolso de un cargo puntual o recurrente

La página Facturas también visualizan un resumen de facturación de la cuente, que incluye el saldo actual y el próximo saldo estimado así como las fechas de la última factura y la próxima factura recurrente.

Complete los siguientes pasos para ver una factura:

1. Seleccione una de las opciones siguientes dependiendo del panel de control que esté utilizando:  
 * Desde el panel de control de Apps o Servicios, pulse **Gestionar** > **Facturación y utilización** > **Facturas**.  
 * Desde el panel de control de Infraestructura, pulse **Cuenta** > **Facturación** > **Facturas**.
2. Puede visualizar una factura en el portal del cliente o descargarla.

## Utilización de servicios de {{site.data.keyword.Bluemix_notm}} con activos de SoftLayer
{: #combined}

Puede utilizar servicios de {{site.data.keyword.Bluemix_notm}} públicos basados en API con sus activos de SoftLayer. Todas las API son seguras y están cifradas para proteger sus datos.

Por ejemplo, ¿ha querido alguna vez añadir capacidades cognitivas de Watson a sus apps que se ejecutan en servidores nativos desde SoftLayer? Puede añadir un servicio como {{site.data.keyword.personalityinsightsshort}} para entender el usuario de la app en cuatro pasos:

1. Busque el servicio en el catálogo.
2. Especifique una instancia del servicio con tan solo unas pulsaciones.
3. Configure el servicio para que se ejecute con el código existente copiando las credenciales del servicio y añadiéndolas a la aplicación.
4. Después de actualizar la app, despliegue la nueva versión en la infraestructura de SoftLayer.

Puede obtener conocimientos sobre Insights and Cognitive invocando las API de Watson desde sus apps en SoftLayer para personalizarlas. O bien, utilice los servicios de Datos y análisis para realizar un análisis más profundo del rendimiento para sus apps. Asimismo, puede seleccionar una base de datos como servicio cuando deje la gestión en manos de {{site.data.keyword.Bluemix_notm}}.

Modernice el desarrollo de sus aplicaciones utilizando contenedores con servicios como {{site.data.keyword.activedeployshort}} y {{site.data.keyword.deliverypipeline}}. Luego puede utilizar el servicio {{site.data.keyword.vpn_short}} para comunicarse con SoftLayer para conectar el contenedor de una red privada a la red privada de SoftLayer. Todos los cargos por uso de los recursos y servicios de cálculo se reflejan en la factura de {{site.data.keyword.Bluemix_notm}}.
