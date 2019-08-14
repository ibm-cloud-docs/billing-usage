---

copyright:
  years: 2019
lastupdated: "2019-06-20"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Métodos recomendados para la facturación y el uso
{: #best-practices}

Siga nuestros métodos recomendados para realizar un seguimiento de los costes y automatizar la facturación en
{{site.data.keyword.Bluemix}}.
{:shortdesc}


## Realizar un seguimiento de los costes de recursos relacionados añadiendo etiquetas
{:#track-billing-tags}

Añada etiquetas a sus recursos para organizar, realizar un seguimiento y gestionar los costes de los recursos relacionados. Cuando utiliza un esquema de etiquetado coherente para identificar qué recursos están vinculados a proyectos específicos, puede agrupar y filtrar por dichas etiquetas al analizar los costes dentro del informe de uso exportado.

1. Etiquete sus recursos utilizando un esquema de etiquetado coherente, como la creación de etiquetas para diferencias centros de coste, centros de datos, proyectos o equipos. Para añadir etiquetas, pulse el icono Menú ![Icono Menú](../icons/icon_hamburger.svg) > **Lista de recursos**. En la columna Etiqueta, pulse **Añadir etiqueta** para cada recurso que desee etiquetar.

   Añada etiquetas en pares clave:valor para añadir columnas personalizadas en función de la clave en el informe de uso. Cree claves basándose en las categorías que utilice para organizar los recursos, como el uso de `costcenter:` para agrupar por centro de coste o
`project:` para agrupar por proyecto.
   {: tip}

   Por ejemplo, puede tener recursos para dos proyectos en una única cuenta, Project ABC y Project XYZ. Project ABC tiene un clúster de {{site.data.keyword.containershort_notm}}, varios despliegues de apps de Cloud Foundry y una base de datos
{{site.data.keyword.cloudant_short_notm}}. Puede añadir la etiqueta `project:abc` a todos estos recursos para distinguir estos recursos para Project ABC de recursos similares en Project XYZ que estén etiquetados con `project:xyz`.

   Para obtener más información sobre la adición y el uso de etiquetas, consulte [Cómo trabajar con etiquetas](/docs/resources?topic=resources-tag).

1. Realice un seguimiento de los costes de los recursos etiquetados exportando el informe de uso para las instancias. Para exportar el informe, vaya a **Gestionar > Facturación y uso**, y seleccione **Uso**. A continuación, pulse **Exportar CSV > Instancia**.

   Utilice la columna Etiquetas del archivo CSV de instancia como ayuda para analizar los recursos en la cuenta. Puede ordenar los datos de CSV de acuerdo con la etiqueta del proyecto en cada instancia para poder analizar mejor el coste de cada proyecto individual. Si ha etiquetado sus recursos con pares clave:valor, también verá columnas en el informe de uso que correspondan con la clave. Por ejemplo, los recursos etiquetados como `project:abc` y `project:xyz` aparecen en la columna Proyecto como `abc` y `xyz`.

   Para obtener más información, consulte
[Visualización del uso](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automatizar la facturación y la gestión del uso utilizando la CLI o las API
{: #billing-cli-apis}

Si desea automatizar la manera en que revisa el uso de sus recursos y los costes asociados, puede utilizar la CLI
[`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) o las API
[Medición del uso ![Icono de enlace externo](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} e [Informes de uso
![Icono de enlace externo](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} para integrar esta funcionalidad en sus propias apps.

Para iniciarse en el uso de las API, configure el
[panel de control de ejemplo de uso de {{site.data.keyword.Bluemix_notm}}
![Icono de enlace externo](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}. Mediante el uso de
{{site.data.keyword.openwhisk}}, el ejemplo implementa un método controlado por API para obtener y visualizar los datos de uso y facturación de
{{site.data.keyword.Bluemix_notm}}.
{: tip}
