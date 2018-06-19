---



copyright:

  years: 2015, 2018
lastupdated: "2018-06-11"

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

Las opciones de facturación y utilización que se visualizan en la consola de {{site.data.keyword.Bluemix_notm}} pueden diferir según si tiene una cuenta Lite o si no tiene una cuenta enlazada.
{: tip}

## Efectuar un pago
{: #makepayment}

Puede realizar un pago puntual siempre que lo desee. El pago puede ser por la totalidad del saldo o un importe parcial. Los detalles que especifique para el pago no se registran. Siga los pasos siguientes para realizar un pago único:

1. Desde la barra de menús, pulse **Gestionar** > **Facturación y utilización** > **Realizar un pago**.  
2. En el campo **Importe del pago**, especifique la cantidad que desea pagar.
3. Seleccione un método de pago:
 * Pago con una tarjeta de crédito. Especifique los detalles y la dirección de facturación de la tarjeta. A continuación, pulse **Realizar pago con tarjeta de crédito**.
 * Pago con PayPal. Especifique sus detalles cuando le sean solicitados para poder completar el pago.

Resuelva cualquier problema que se le pueda presentar al efectuar el pago. El saldo de la cuenta se actualizará una vez el pago se haya aceptado. Puede ponerse en contacto con el equipo de soporte pulsando **Soporte** > **Añadir incidencia**.

## Cambiar su método de pago
{: #changepaymethod}

Cada cuenta facturable debe tener una tarjeta de crédito registrada que sea válida. Cada mes, se cargará en la tarjeta de crédito la cantidad utilizada que se acumule durante dicho mes. En la consola {{site.data.keyword.Bluemix_notm}}, complete los siguientes pasos para añadir o cambiar sus detalles de pago:

1. Desde la barra de menús, pulse **Gestionar** > **Facturación y uso** > **Modificar método de pago**.  
2. En la sección Añadir método de pago, especifique los detalles y la dirección de facturación de la tarjeta de crédito. A continuación, pulse **Añadir tarjeta de crédito**.

Se validarán los detalles de la tarjeta y estará disponible para utilizarse en su cuenta en 24 horas. Se enviará un correo electrónico de confirmación al contacto especificado en la sección de la dirección de facturación de la tarjeta.

## Visualizar los artículos facturados
{: #viewbilling}

Puede asociar o eliminar la asociación de elementos de facturación en dispositivos específicos. De forma predeterminada, la página de **Artículos de facturación** visualiza los artículos de facturación asociados. La vista se puede cambiar seleccionando una opción desde el menú de visualización. Puede asociar o eliminar la asociación de un elemento o utilizar la operación Acciones masivas para asociar o eliminar la asociación de varios elementos al mismo tiempo. También puede cancelar elementos de facturación en cualquier momento. 

1. Seleccione el **icono de Menú![Icono de menú](../icons/icon_hamburger.svg) > opción Infraestructura**. 
2. Desde la barra de menús, pulse **Cuenta** > **Facturación** > **Artículos de facturación**.
3. Para filtrar la vista, seleccione una opción de elemento de facturación de la lista.

## Visualizar facturas
{: #viewinvoices}

Puede ver o pagar sus facturas siempre que lo desee. Cada factura viene resumida con su Número de factura, Fecha, Tipo de factura y varios saldos monetarios. Los tipos de facturación se describen en la lista siguiente:

 *  Nueva: la primera factura de una serie recurrente de facturas
 *  Recurrente: una factura de cargos recurrentes que llevan activos en la cuenta más de un mes
 *  Cargo puntual: un cargo puntual de distintos gastos, que pueden incluir los sobrecostes
 *  Cargo: un cargo de {{site.data.keyword.Bluemix_notm}} en el saldo de su cuenta
 *  Devolución: una devolución o desembolso de un cargo puntual o recurrente

La página **Facturas** también muestra un resumen de facturación de la cuenta, que incluye el saldo actual y estimado, el método de pago y las fechas de la última factura y la próxima factura recurrente.

Complete los siguientes pasos para ver una factura:

1. Seleccione el **icono de Menú![Icono de menú](../icons/icon_hamburger.svg) > opción Infraestructura**. 
2. Desde la barra de menús, pulse **Cuenta** > **Facturación** > **Facturas**.
3. Puede visualizar una factura en el portal del cliente o descargarla.

## Utilización de servicios de {{site.data.keyword.Bluemix_notm}} con activos de SoftLayer
{: #combined}

Puede utilizar servicios de {{site.data.keyword.Bluemix_notm}} públicos basados en API con sus activos de SoftLayer. Todas las API son seguras y están cifradas para proteger sus datos.

Por ejemplo, ¿desea añadir capacidades cognitivas de Watson a las apps que se ejecutan en servidores nativos desde SoftLayer? Puede añadir un servicio como {{site.data.keyword.personalityinsightsshort}} para entender el usuario de la app en cuatro pasos:

1. Busque el servicio en el catálogo.
2. Especifique una instancia del servicio con tan solo unas pulsaciones.
3. Configure el servicio para que se ejecute con el código existente copiando las credenciales del servicio y añadiéndolas a la aplicación.
4. Después de actualizar la app, despliegue la nueva versión en la infraestructura de SoftLayer.

Puede obtener conocimientos sobre Insights and Cognitive invocando las API de Watson desde sus apps en SoftLayer para personalizarlas. O bien, utilice los servicios de Datos y análisis para realizar un análisis del rendimiento para sus apps. Asimismo, puede seleccionar una base de datos como servicio cuando deje la gestión en manos de {{site.data.keyword.Bluemix_notm}}.

Modernice el desarrollo de sus aplicaciones utilizando contenedores con servicios como {{site.data.keyword.activedeployshort}} y {{site.data.keyword.deliverypipeline}}. Luego puede utilizar el servicio {{site.data.keyword.vpn_short}} para comunicarse con SoftLayer para conectar el contenedor de una red privada a la red privada de SoftLayer. Todos los cargos por uso de los recursos y servicios de cálculo se reflejan en la factura de {{site.data.keyword.Bluemix_notm}}.
