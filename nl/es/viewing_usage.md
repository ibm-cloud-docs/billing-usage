---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Visualización del uso
{: #viewingusage}

Puede ver los detalles de uso, incluido un resumen de los cargos estimados para todos los recursos, servicios y planes de soporte que se utilizan al mes en sus organizaciones, en la página Uso de la consola de {{site.data.keyword.Bluemix}}.
{:shortdesc}

Los gestores de facturación solo pueden ver los detalles de las organizaciones en las que tienen asignado el rol de Gestor de facturación. 
{: note}


## Visualización de permisos de uso
{: #view-usage-permissions}

Para los recursos gestionados por Cloud Foundry, se debe aplicar el rol de Gestor de facturación al nivel de organización. Para ver el uso de recursos de {{site.data.keyword.Bluemix}} Identity and Access Management (IAM), se debe aplicar el rol de Visor al grupo de recursos. Para obtener más información sobre los roles de permisos, consulte [Acceso de IAM](/docs/iam/users_roles.html#userroles), [Acceso a Cloud Foundry](/docs/iam/cfaccess.html#cfaccess) o [Permisos de la infraestructura clásica](/docs/iam/infrastructureaccess.html#infrapermission).

## Visualización de detalles de uso de servicio 
{: #services}

En la sección de servicios, puede ver una lista de sus servicios y los costes estimados asociados a dichos servicios. Para ver un resumen de los cargos estimados para todas las instancias de un recurso específico, siga estos pasos: 

1. Vaya a **Gestionar > Facturación y uso** y seleccione **Uso**. 
2. Pulse **Ver instancias** para ver todas las instancias de un tipo específico de recurso.  
3. Para ver un resumen detallado de los cargos estimados para cada instancia de un tipo de recurso específico, pulse **Ver detalles de la instancia**. También puede ver las métricas detalladas de uso mensual para la instancia seleccionada. 

La cuenta se factura al propietario por el uso total en el que han incurrido todas las organizaciones al final de cada ciclo de facturación. Cada ciclo de factura dura un mes.

Los propietarios de cuentas pueden filtrar el resumen de uso por grupo y seleccionar el intervalo de tiempo del uso. Los cargos mostrados representan la cantidad que se le factura a usted, como propietario de cuenta, para dicho mes.

Si selecciona una organización específica de la lista **Filtrar por grupo**, puede ver la utilización total para esa organización, incluido cualquier uso como parte de un nivel gratuito. El uso de nivel gratuito se muestra como gratuito a nivel de cuenta, pero no a nivel organizativo. Cuando visualice el uso de la organización, verá el uso real de esa organización, incluido el uso gratuito y de pago. Todo el uso de la organización se acumula en el uso de la cuenta una vez que se haya eliminado el nivel gratuito.

El gestor de una cuenta de pago según uso puede establecer notificaciones de gasto relativas al coste total de su cuenta, para su tiempo de ejecución y servicios y para los servicios individuales, sin incluir servicios de terceros. Para obtener más información, consulte el apartado [Configuración de notificaciones de gastos](/docs/billing-usage/notifications.html).

## Exportación de los detalles de uso a un archivo `.csv`
{: #export-csv}

Puede exportar un resumen de su uso o información sobre sus servicios e instancias en un archivo CSV. Si exporta el archivo CSV, puede buscar fácilmente estimaciones de uso y de costes para cada recurso, para saber lo que debe cobrar a los clientes o para comprender mejor sus costes. 

1. Vaya a **Gestionar > Facturación y uso** y seleccione **Uso**.
2. Pulse **Exportar CSV**.  


