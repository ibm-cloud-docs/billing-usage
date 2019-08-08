---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise billing, enterprise, subscription, billing unit, billing option, invoice, credit pool

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}

# Gestión centralizada de facturación y uso de empresas
{: #enterprise}

Las empresas le permiten gestionar de forma centralizada varias cuentas de {{site.data.keyword.Bluemix}}. Debido a que la facturación es independiente de las cuentas secundarias individuales y se consolida a nivel de empresa, las empresas simplifican la gestión de la facturación, y los pagos para las cuentas.
{: shortdesc}

¿No conoce las empresas de {{site.data.keyword.Bluemix_notm}}? Consulte [¿Qué es una empresa?](/docs/account?topic=account-enterprise) para obtener más detalles sobre cómo las empresas pueden ayudarle a gestionar de forma centralizada la facturación y el uso.
{: tip}

## Modelo de facturación de empresa
{: #enterprise-billing-basics}

En una empresa, la facturación se gestiona en la empresa en lugar de en las cuentas secundarias individuales. Este modelo centralizado de facturación difiere de una cuenta autónoma en lo siguiente.

 * El crédito de las suscripciones o promociones de las cuentas que se añaden a la empresa se consolida en la agrupación de crédito de la empresa. El administrador de facturación añade las nuevas suscripciones a la agrupación de crédito de la cuenta de empresa.
 * El uso de todas las cuentas se deduce de la agrupación de crédito compartida. Si tienen acceso, los usuarios de empresa pueden ver los costes de uso de todas las cuentas y grupos de cuentas de la empresa. Los usuarios dentro de cada cuenta secundaria pueden seguir supervisando el uso en la cuenta en particular, pero no pueden ver las otras cuentas de la empresa.
 * El uso se factura a través de la cuenta de empresa. Sólo el administrador de facturación de la empresa puede ver las facturas y gestionar los pagos.

<figure>
<a href="https://{DomainName}/docs/api/content/billing-usage/images/enterprise-billing-usage.svg">
<img src="images/enterprise-billing-usage.svg" alt="Un diagrama que muestra que el crédito de las cuentas se añade a la agrupación de crédito de la empresa, que gestiona el administrador de facturación, el acceso de los usuarios se gestiona aparte y puede direccionarse a la empresa, a un grupo de cuentas o a una cuenta."></a>
<figcaption>Figura 1. Facturación y gestión de uso de una empresa</figcaption>
</figure>

## Opciones de facturación
{: #enterprise-billing-options}

Las empresas requieren una facturación de suscripción, lo que significa que se compra una suscripción para una cantidad de crédito que se debe gastar durante el período de suscripción, y el uso se deduce del crédito de suscripción a una tasa de descuento. La cuenta que se utiliza para crear la empresa debe ser una [Cuenta de suscripción](/docs/account?topic=account-accounts#subscription-account). Una vez que se ha creado la empresa, puede añadir cualquier tipo de cuenta a la empresa. Si añade una cuenta Lite o de prueba, se actualiza automáticamente a una cuenta de Pago según uso.

Cada empresa admite únicamente una sola moneda de facturación. Todas las cuentas deben utilizar la moneda de facturación de empresa para poder añadirlas a la empresa.
{: note}

Las cuentas que se añaden a la empresa dejan de gestionar su facturación por separado. Como resultado, no se puede añadir crédito de suscripción a cuentas hijo individuales. El crédito de suscripción debe añadirse a la cuenta de empresa, donde se pasa a ser parte de la agrupación de crédito de empresa.

### Transición de facturación al agregar cuentas
{: #billing-transition}

Cuando se añade una cuenta existente a una empresa, sus transiciones de facturación las gestiona la cuenta de empresa. Esta transición incluye los siguientes cambios en la cuenta.

   * Para las cuentas de suscripción que se añaden, el tipo de cuenta se cambia a Pago según uso. Este cambio refleja que la cuenta no tiene sus propias suscripciones, pero que todavía tiene acceso completo a servicios facturables preparados para la producción.
   * Las suscripciones y promociones de cada cuenta se trasladan a la cuenta de empresa, donde pasan a formar parte de la agrupación de crédito. Después de la acción de mover, cada suscripción tiene el mismo período de crédito y de plazo, pero se le da un nuevo ID exclusivo.
   * El acceso a la información de facturación y pago para futuros periodos de facturación está limitado a los usuarios de la cuenta de empresa. Los usuarios de una cuenta secundaria no pueden acceder a la información de facturación y de pago, como por ejemplo facturas, pagos o suscripciones, aunque anteriormente tuvieran acceso a la cuenta. Para ver o gestionar la facturación, los usuarios tienen que ser invitados a la cuenta de empresa y se les tiene que dar acceso al servicio de Facturación de esa cuenta.
   * El uso se factura a la cuenta de empresa durante todo el mes en que se ha añadido la cuenta. Por ejemplo, si añade una cuenta a la empresa el 15 de junio, en la factura de julio se refleja todo el uso del mes de junio.

### Agrupación de crédito compartido
{: #credit-pool}

La agrupación de crédito de empresa consolida el crédito de todas las cuentas de la empresa y lo comparte con las cuentas. La agrupación incluye el crédito de todas las fuentes, incluyendo el crédito de suscripción a la plataforma, el crédito promocional y el crédito de soporte. Cuando las cuentas de la empresa crean y utilizan recursos, el coste de este uso se deduce de la agrupación de crédito.

El administrador de facturación de la cuenta de empresa puede ver y supervisar la cantidad total de crédito disponible en el panel de control de la empresa. Si se necesita más crédito para cubrir el uso de la empresa, se puede adquirir una nueva suscripción y luego añadirla a la cuenta de empresa. Las suscripciones sólo se pueden añadir a la cuenta de empresa y no a otras cuentas de la empresa.

Debido a que las suscripciones se pueden dimensionar para toda la empresa en lugar de por cuenta, obtiene las siguientes ventajas:
   * Dimensionamiento de la suscripción más simple porque las suscripciones se aplican a más de una cuenta
   * Mejores descuentos en los costes de uso porque las suscripciones son más grandes
   * Menos fechas de vencimiento de las que realizar el seguimiento y la gestión después cuando caduquen las suscripciones existentes

En una empresa, las suscripciones se gestionan desde la cuenta de empresa de igual modo que para una cuenta autónoma. Consulte [Gestión de suscripciones](/docs/billing-usage?topic=billing-usage-subscriptions) para obtener más información sobre la gestión de la plataforma y las suscripciones de soporte.

## Informes de uso
{: #enterprise-usage-reporting}

Las empresas proporcionan informes de uso de arriba abajo para poder realizar un seguimiento de los costes del uso de recursos de todas las cuentas de la empresa. Partiendo del nivel de empresa, puede navegar dentro de la estructura de la empresa para ver los costes de uso estimados dentro de cada cuenta o grupo de cuentas. En el nivel de cuentas, los usuarios de empresa pueden ver los costes de cada tipo de recurso o servicio de la cuenta.

Los administradores de empresa pueden proporcionar acceso granular a los usuarios de modo que puedan ver el uso sólo para determinadas cuentas o grupos de cuentas. Por ejemplo, imagine que su empresa tiene grupos de cuentas para cada departamento, y cada departamento tiene grupos de cuentas para cada equipo.
   * Da acceso a su agente financiero para ver toda la empresa, de modo que pueda realizar un seguimiento y recuperar los costes de cada departamento.
   * Da acceso a cada jefe de departamento para ver el uso de todo en el grupo de cuentas de su departamento.
   * Da acceso a cada jefe de equipo para ver sólo las cuentas en el grupo de cuentas de su equipo.

Dado que el acceso a la empresa es independiente del acceso a cada cuenta, los usuarios de empresa no pueden gestionar automáticamente recursos dentro de las cuentas secundarias. De forma similar, los usuarios de cada cuenta pueden seguir viendo su uso pasado y actual desde la página de Uso independientemente de si tienen acceso de empresa.

Puede ver el uso desde la página Uso de la consola, desde la CLI, o desde la API de Enterprise Usage Reports. Consulte [Visualización del uso en una empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage) para obtener más información.

## Facturación y pagos
{: #enterprise-invoicing}

El uso en la empresa se factura a través de la cuenta de empresa.  Al igual que con todas las cuentas facturables, el uso se factura mensualmente, y la factura vence en la fecha de facturación de la cuenta. Durante cada ciclo de facturación, se facilita una sola factura con los costes de uso de todas las cuentas en la cuenta de empresa. La factura contiene los costes de toda la plataforma y el uso de la infraestructura en una sola línea de detalle de la factura. Si se utiliza todo el crédito de la agrupación de crédito, la factura contiene una línea de detalle para los cargos de excedente.

Debido a que todo el uso se factura a través de la cuenta de empresa, las cuentas secundarias dentro de la empresa no reciben facturas separadas.

Puede analizar los costes de uso de cada cuenta o grupo de cuentas en la página 'Uso' de la cuenta de empresa. Para obtener detalles, consulte [Visualización del uso en una empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).
{: tip}

## Gestión del acceso para la facturación y el uso en la empresa
{: #enterprise-billing-access}

Al igual que con otros roles de gestión de empresa, el acceso a facturación y el uso de la empresa se gestiona a través de la cuenta de empresa. Los usuarios deben ser invitados a la cuenta de empresa y se les debe asignar una política de acceso con un rol en el servicio deseado.

En una empresa, el acceso de facturación y el acceso de uso se asignan por separado.

   * El acceso de facturación se proporciona asignando a los usuarios de empresa un rol en el servicio de Facturación. Por ejemplo, puede asignar el rol de Visor a un usuario de empresa para que pueda ver la cantidad de crédito de suscripción disponible en la agrupación de crédito, o puede asignar el rol Editor o Administrador para que pueda añadir nuevas suscripciones o gestionar métodos de pago.
   * El acceso de uso se proporciona asignando a usuarios de empresa el rol de Visor, Editor o Administrador de informes de uso en el servicio de Empresa. Puede asignar este acceso para toda la empresa o para cuentas o grupos de cuentas específicos.

Si desea que el administrador de facturación pueda ver los costes por cuenta o grupo de cuentas, asegúrese de asignarles el acceso adecuado tanto en el servicio de Empresa como en el servicio de Facturación.
{: tip}

Para obtener más información, consulte [Gestión de usuarios y del acceso para empresas](/docs/iam?topic=iam-enterprise-access).
