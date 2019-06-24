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


# Traitement des incidents liés à la gestion de la facturation et de l'utilisation
{: #troubleshoot}

Les problèmes d'ordre général relatifs à la gestion de la facturation et de l'utilisation peuvent nécessité que l'autorité requise accède vos informations de facturation. Dans de nombreux cas, ce type de problème peut être résolu en quelques opérations simples.
{:shortdesc}


## Pourquoi ne puis-je pas accéder aux informations de facturation ?
{: #cannot-access-billing-info}
{: troubleshoot}

Lorsque vous tentez d'accéder à vos informations de facturation (paiements et factures, par exemple), un message d'erreur s'affiche indiquant que la fonction n'est pas disponible.
{: tsSymptoms}

Cette situation survient si vous ne disposez pas de l'autorisation vous permettant d'afficher les informations de facturation pour le compte. Vous devez être propriétaire d'un compte, responsable de la facturation d'organisation Cloud Foundry ou disposer d'une règle IAM pour tous les services de gestion de compte avec le rôle Administrateur affecté.
{: tsCauses}

Vous pouvez consulter les informations de facturation de tout compte dont vous êtes propriétaire. Un responsable de la facturation peut afficher les informations de facturation concernant une organisation Cloud Foundry. De plus, pour les ressources gérées par IAM, vous devez disposer d'une règle IAM concernant tous les services de gestion de compte avec le rôle Administrateur affecté.

Vérifiez votre accès en procédant comme suit :

  1. Accédez à **Gérer > Accès (IAM)** puis sélectionnez **Utilisateurs**.
  2. Cliquez sur votre nom sur la page Utilisateurs.
  3. Cliquez sur **Règles d'accès** pour afficher vos règles d'accès IAM affectées.
  4. Cliquez sur **Accès Cloud Foundry** et développez les lignes pour vos organisations affectées afin de voir si vous disposez du rôle de propriétaire de compte ou de responsable de la facturation.

Pour plus d'informations sur l'accès IAM, voir [Rôles Cloud IAM](/docs/iam?topic=iam-userroles). Pour plus d'informations sur l'accès Cloud Foundry, voir [Rôles Cloud Foundry](/docs/iam?topic=iam-cfaccess).
{: tsResolve}


## Pourquoi ne puis-je pas appliquer un code de fonction ?
{: #cannot-apply-feature-code}
{: troubleshoot}

Lorsque vous tentez d'appliquer un code de fonction, une erreur s'affiche, indiquant que le code ne peut pas être appliqué.
{: tsSymptoms}

Votre compte ne satisfait pas les exigences du code de fonction, ou vous ne disposez pas du niveau d'accès requis dans le compte.
{: tsCauses}

- Vérifiez que vous disposez du type de compte approprié. Par exemple, certains comptes de fonction concernant des promotions pédagogiques sont réservés aux comptes Lite. Pour afficher votre type de compte, accédez à **Gérer > Compte** puis sélectionnez **Paramètres de compte**. Pour plus de détails, voir [Application de codes de fonction](/docs/account?topic=account-codes).
- Vérifiez que vous disposez de l'accès pour appliquer le code de fonction. Pour cela, vous devez au moins disposer d'un rôle éditeur sur l'ensemble des services de gestion de compte. Pour vérifier ou changer des rôles, voir [Affectation de l'accès aux services de gestion de compte](/docs/iam?topic=iam-account-services).
{: tsResolve}
