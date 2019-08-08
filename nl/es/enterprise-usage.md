---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:external: target="_blank" .external}
{:note: .note}


# Visualización del uso en una empresa
{: #enterprise-usage}

Puede realizar un seguimiento de los costes de los recursos y el soporte de las cuentas de una empresa de {{site.data.keyword.Bluemix}} visualizando su uso. Las cuentas y grupos de cuentas de los que puede ver el uso dependen del acceso que tenga asignado.
{: shortdesc}

Las empresas de {{site.data.keyword.Bluemix_notm}} le permiten gestionar de forma centralizada varias cuentas de {{site.data.keyword.Bluemix_notm}}. Como usuario de empresa, puede vigilar el uso de recursos y los costes asociados de cualquier cuenta en la empresa. Consulte [¿Qué es una empresa?](/docs/account?topic=account-enterprise) para obtener más información.

## Acceso necesario para ver el uso de una empresa
{: #enterprise-usage-access}

En una empresa, el acceso a la información de uso lo controla el servicio de empresa. Para ver la información de uso, los usuarios deben haber sido invitados a la cuenta de empresa y tener el rol de visor, editor o administrador de informes de uso en el servicio de empresa. El rol de Visor de informes de uso proporciona acceso unicamente para ver informes de uso, mientras que los roles de Editor y Administrador permiten acciones adicionales de gestión de la empresa. Para ajustarse a las mejores prácticas en cuanto a seguridad, asigne la menor cantidad de acceso necesario para que el usuario pueda completar su tarea. Para obtener más información, consulte [Acciones y roles de empresa](/docs/iam?topic=iam-account-services#enterprise-account-management).

Puede otorgar a los usuarios acceso granular para que puedan ver el uso de una determinada cuenta o grupo de cuentas. Por ejemplo, imagine que su empresa tiene grupos de cuentas para cada departamento, y cada departamento tiene grupos de cuentas para cada equipo. Puede definir el ámbito de acceso para que cada usuario de empresa pueda ver sólo la información que necesita para cumplir su rol de trabajo.
   * El responsable financiero necesita ver el uso de toda la empresa para poder realizar un seguimiento y recuperar los costes de cada departamento, pero no necesitan crear cuentas ni grupos de cuentas. Puede asignarle el rol de Visor de Informes de uso de la empresa.
   * Cada jefe de departamento necesita ver el uso de su departamento, y también necesita crear y gestionar cuentas y grupos de cuentas para sus equipos. Asigne a cada jefe de departamento el rol de Editor para el grupo de cuentas de su departamento.
   * Cada jefe de equipo necesita ver el uso de su equipo, pero también tienen que obtener la aprobación del departamento para agregar nuevas cuentas a su equipo. Asigne a cada jefe de equipo el rol de Visor de informes de uso para el grupo de cuentas de su equipo. Pueden ver el uso de todas las cuentas dentro del grupo de cuentas, pero no el uso de los grupos de cuentas de otros equipos del departamento.

Para conocer los pasos detallados para asignar el acceso de empresa, consulte [Asignación de acceso de empresa](/docs/iam?topic=iam-assign-access-enterprise).

## Visualización del uso de empresa
{: #enterprise-usage-console}

1. Inicie la sesión en la cuenta de empresa.
1. Vaya a **Gestionar > Facturación y uso** y seleccione **Uso**.

   La página Uso muestra los costes de todo el uso de recursos de la empresa, desglosados por cuenta y grupo de cuentas. También puede ver el uso del crédito de soporte de toda la empresa y cualquier exceso en el que se haya incurrido.

   No se incluye la información de uso de los servicios de infraestructura clásica para el periodo de facturación actual. Sin embargo, sí se incluye la de los periodos de facturación anteriores, que puede ver seleccionando un mes anterior en el menú **Intervalo de tiempo**. Para obtener más información, consulte [Visualización del uso de recursos de la infraestructura clásica](/docs/billing-usage?topic=billing-usage-infra-usage).
1. Para ver el uso dentro de un grupo de cuentas, pulse en el nombre del grupo de cuentas en la tabla o en el menú **Nivel de empresa**. De forma similar al nivel de empresa, el uso se desglosa por cuenta y grupo de cuentas.

   Si un grupo de cuentas no contiene ninguna cuenta, no se muestra en la página Uso.

1. Para ver el uso por recurso, vaya al nivel de cuenta pulsando en los grupos de cuentas de la tabla o seleccionando la cuenta desde el menú **Nivel de empresa**. Se muestran los costes de cada tipo de recurso que se ha utilizado durante el período de tiempo.

   Desde la cuenta de empresa, no se pueden ver los datos de uso del plan de recursos ni de la instancia porque se requiere acceso dentro de la cuenta. Si usted es un usuario en la cuenta, cambie a la cuenta para ver estos datos. Necesita acceso de facturación a los recursos y servicios de la cuenta tal como se describe en [Visualización del uso](/docs/billing-usage?topic=billing-usage-viewingusage).

En la cuenta de empresa sólo se visualizan los datos de uso en los que incurren las cuentas de la empresa. Para ver el uso desde antes de añadir una cuenta a la empresa, inicie sesión en dicha cuenta y seleccione el intervalo de tiempo correspondiente.
{: note}

### Visualización del uso de la empresa utilizando la CLI
{: #enterprise-usage-cli}

Puede obtener un informe de uso de la empresa, de un grupo de cuentas o de una cuenta específica.

1. Inicie sesión y seleccione la cuenta de empresa.

   ```
   ibmcloud login
   ```
   {:codeblock}

1. Si desea ver el uso de un grupo de cuentas o de una cuenta específica, busque el nombre o el ID ejecutando el mandato **`ibmcloud enterprise`**.

   Por ejemplo, el mandato siguiente muestra todos los grupos de cuentas de una empresa.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. Visualice el uso ejecutando el mandato **`ibmcloud billing`** como se muestra en los ejemplos siguientes.

   * Ver el uso de toda la empresa para el mes actual.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * Ver el uso para el grupo de cuentas `Development` de julio de 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {:codeblock}

   * Ver el uso de los grupos de cuentas y las cuentas que están directamente bajo la empresa.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:codeblock}

   De forma predeterminada, los mandatos de salida del informe de uso del mes actual se encuentran en el formato siguiente. La mayoría de los costes se listan como costes facturables. Los costes no facturables sólo se listan en casos extraordinarios, como por ejemplo los del mes cuando se añade una cuenta de prueba a la empresa.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month   
Example Corp     account         123.45          0                   USD        2019-07   
Development      account_group   234.56          0                   USD        2019-07   
Marketing        account_group   345.67          0                   USD        2019-07   
Sales            account_group   456.78          0                   USD        2019-07
   ```

   Puede generar el informe en formato JSON especificando la opción `--output JSON`.
   {: tip}

### Visualización del uso de la empresa utilizando la API
{: #enterprise-usage-api}

Puede obtener informes de uso de una empresa y de sus cuentas llamando a la <!-- [Enterprise Usage Reports API (Beta)](https://{DomainName}/apidocs/enterprise-apis/resource-usage-reports){: external} --> API de Enterprise Usage Reports (Beta). Puede basar la consulta de la llamada de API en una empresa, en un grupo de cuentas o en una cuenta y especificar si se debe ver la entidad o sus hijos. La API de Enterprise Usage Reports es un release beta.

Los ejemplos siguientes muestran las consultas que puede utilizar para obtener diferentes informes de uso. En la llamada a la API, sustituya las variables de ID y la señal IAM por los valores de la empresa.

Ver el uso de toda la empresa para el mes actual.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Ver el uso de un grupo de cuentas para julio de 2019.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?account_group_id=$ACCOUNT_GROUP_ID&month=2019-07" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}

Ver el uso de los grupos de cuentas y las cuentas directamente bajo la empresa.

```
curl -X GET \
"https://enterprise.test.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=$ENTERPRISE_ID&children=true" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json'
```
{: codeblock}


## Recuperación de costes del uso de empresa
{: #enterprise-cost-recovery}

Una empresa consolida la facturación de todas sus cuentas y grupos de cuentas en una sola factura, lo que simplifica la gestión de la facturación. Puede recuperar los costes del uso de recursos de la empresa cargando los costes de uso para cada cuenta o grupo de cuentas en el departamento o equipo asociado.

Para ver la jerarquía de empresa y el uso, necesita una política de acceso con el rol Editor o Administrador en el servicio de Empresa para toda la empresa. En los pasos siguientes se utiliza la consola de {{site.data.keyword.Bluemix_notm}} como ejemplo, pero también puede llevar a cabo estos pasos utilizando la CLI o la API.

1. Busque los costes de uso de cada departamento, yendo a **Gestionar > Uso** en la cuenta de empresa. En el menú **Intervalo de tiempo**, seleccione el mes anterior para ver el uso que se incluye en la última factura.

  Los costes de los grupos de cuentas se listan en la tabla. Estos costos incluyen todos los cargos sin impuestos cargados en su región de facturación. Si desea un mayor desglose de los costes de uso, pulse en el nombre del grupo de cuentas para ver las cuentas y los grupos de cuentas que contiene.

1. Identifique los departamentos dentro de la compañía que corresponden a los grupos de cuentas.

   Si los contactos que se han asignado a los grupos de cuentas están asociados con el departamento del que desea recuperar los costes, buscar el contacto es una forma de encontrar esta información. Vaya a **Gestionar > Empresa** y seleccione **Cuentas**. En la tabla se lista el contacto de cada grupo de cuentas.

   Sin embargo, las prácticas de facturación varían según la empresa. Por ejemplo, el contacto del grupo de cuentas puede ser un contacto técnico que no esté asociado con el departamento al que desea facturar. Compruebe siempre el departamento correcto según los procesos de contabilidad de la empresa.

   Si su empresa utiliza códigos de facturación para facturar los costes a los departamentos, añada el código de facturación al nombre del grupo de cuentas para identificar fácilmente el código. Por ejemplo, `Sales - A2B3`.
   {: tip}

1. Empareje los costes de uso de cada grupo de cuentas con el departamento identificado, y siga los procesos de la empresa para enviar los cargos.
