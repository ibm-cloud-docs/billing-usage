---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-11"

keywords: troubleshoot billing, billing error, payment error, error message, feature code, subscription code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Resolución de problemas de gestión de la facturación y el uso
{: #troubleshoot}

Los problemas generales de gestión de la facturación y el uso de {{site.data.keyword.cloud}} pueden incluir la autoridad necesaria para acceder a la información de facturación. En muchos casos, puede solucionar el problema siguiendo unos sencillos pasos.
{:shortdesc}


## ¿Por qué no puedo acceder a mi información de facturación?
{: #cannot-access-billing-info}
{: troubleshoot}

Cuando intenta acceder a la información de facturación, como por ejemplo pagos y facturas, obtiene un mensaje que indica que la función no está disponible.
{: tsSymptoms}

Este mensaje se recibe porque no tiene autorización para ver la información de facturación de la cuenta. Debe ser el propietario de la cuenta o el gestor de facturación de la organización de Cloud Foundry o debe tener una política de IAM sobre todos los servicios de gestión de la cuenta con el rol de administrador asignado.
{: tsCauses}

Puede ver la información de facturación sobre cualquier cuenta de la que sea propietario. Un gestor de facturación puede ver la información de facturación de una organización de Cloud Foundry. Y, para los recursos habilitados para IAM, debe tener una política de IAM sobre todos los servicios de gestión de la cuenta con el rol de Administrador asignado.

Para comprobar su acceso, siga los pasos siguientes:

  1. Vaya a **Gestionar > Acceso (IAM)** y seleccione **Usuarios**.
  2. Pulse su nombre en la página Usuarios.
  3. Pulse **Políticas de acceso** para ver las políticas de acceso de IAM asignadas.
  4. Pulse **Acceso a Cloud Foundry** y expanda las filas de las organizaciones asignadas para ver si tiene un rol de Propietario de la cuenta o de Gestor de facturación.

Para obtener más información sobre el acceso de IAM, consulte [Roles de Cloud IAM](/docs/iam?topic=iam-userroles). Y, para obtener más información sobre el acceso de Cloud Foundry, consulte [Roles de Cloud Foundry](/docs/iam?topic=iam-cfaccess).
{: tsResolve}


## ¿Por qué no puedo aplicar un código de característica?
{: #cannot-apply-feature-code}
{: troubleshoot}

Cuando intenta aplicar un código de característica, ver un error que indica que no se puede aplicar el código.
{: tsSymptoms}

La cuenta no cumple los requisitos para el código de característica, o bien no tiene el nivel de acceso necesario en la cuenta.
{: tsCauses}

- Compruebe que tiene el tipo de cuenta correcto. Por ejemplo, algunos códigos de característica correspondientes a promociones educativas solo son para cuentas Lite. Para ver el tipo de cuenta, vaya a **Gestionar > Cuenta** y seleccione **Valores de cuenta**. Para obtener más información, consulte [Aplicación de códigos de característica](/docs/account?topic=account-codes).
- Compruebe que tiene acceso para aplicar el código de característica. Para aplicar cualquier código de característica, debe tener el rol de Editor o superior sobre todos los servicios de gestión de la cuenta. Para revisar o cambiar roles, consulte [Asignación de acceso a los servicios de gestión de cuentas](/docs/iam?topic=iam-account-services).
{: tsResolve}
