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


# Troubleshooting for managing billing and usage
{: #troubleshoot}

General problems with managing your billing and usage might include the required authority to access your billing information. In many cases, you can recover from the problem by following a few easy steps.
{:shortdesc}


## Why can't I access billing information?
{: #cannot-access-billing-info}
{: troubleshoot}

When you try to access your billing information, such as payments and invoices, you get a message that says the function isn't available.
{: tsSymptoms}

You will get this message because you don't have authorization to view the billing information for the account. You must be an account owner, Cloud Foundry org billing manager, or have an IAM policy on all account management services with the administrator role assigned.
{: tsCauses}

You can view billing information on any account that you're an account owner. A billing manager is able to view billing information for a Cloud Foundry organization. And, for IAM-enabled resources, you must have an IAM policy on all account management services with the Administrator role assigned.

Check your access by completing the following steps:

  1. Go to **Manage > Access (IAM)**, and select **Users**.
  2. Click your name from the Users page.
  3. Click **Access policies** to view your assigned IAM access policies.
  4. Click **Cloud Foundry access** and expand the rows for your assigned orgs to see whether you have an Account owner or Billing manager role.

For more information about IAM access, see [Cloud IAM roles](/docs/iam?topic=iam-userroles). And, for more information about Cloud Foundry access, see [Cloud Foundry roles](/docs/iam?topic=iam-cfaccess).
{: tsResolve}


## Why can't I apply a feature code?
{: #cannot-apply-feature-code}
{: troubleshoot}

When you try to apply a feature code, you see an error that states that the code cannot be applied.
{: tsSymptoms}

Your account doesn't meet the requirements for the feature code, or you don't have the required access level in the account.
{: tsCauses}

- Verify you have the correct account type. For example, some feature codes for educational promotions are only for Lite accounts. To view your account type, go to **Manage > Account**, and select **Account settings**. For details, see [Applying feature codes](/docs/account?topic=account-codes).
- Verify that you have access to apply the feature code. To apply any feature code, you must have an Editor role or higher on all account management services. To review or change roles, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).
{: tsResolve}
