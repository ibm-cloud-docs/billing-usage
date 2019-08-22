---

copyright:
  years: 2017, 2019
lastupdated: "2019-08-21"

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

General problems with managing your {{site.data.keyword.cloud}} billing and usage might include the required authority to access your billing information. In many cases, you can recover from the problem by following a few easy steps.
{:shortdesc}


## Why can't I access billing information?
{: #cannot-access-billing-info}
{: troubleshoot}

When you try to access your billing information, such as payments and invoices, you get a message that says the function isn't available.
{: tsSymptoms}

You see this message because you don't have authorization to view the billing information for the account.
{: tsCauses}

To manage invoices and payments, you need an IAM access policy with the Operator role or higher on the Billing account management service. To view usage information for the entire account, you need the Administrator role on the Billing service. Account owners can always view billing information for the account.

Check your access by completing the following steps:
{: tsResolve}

  1. Go to **Manage > Access (IAM)**, and select **Users**.
  2. Click your name from the Users page.
  3. Click **Access policies** to view your assigned IAM access policies.
  4. If you don't have the required access, contact the account owner to request it.

For more information about account management services, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).

## Why can't I apply a subscription or feature code?
{: #cannot-apply-feature-code}
{: troubleshoot}

When you try to apply a subscription or feature code, you see an error that states that the code cannot be applied.
{: tsSymptoms}

Your account doesn't meet the requirements for the feature code, or you don't have the required access in the account.
{: tsCauses}

- Verify that you have the correct account type. For example, some feature codes for educational promotions are only for Lite accounts. To view your account type, go to **Manage > Account**, and select **Account settings**. For more information, see [Applying feature codes](/docs/account?topic=account-codes).
- Verify that you have access to apply the code. To apply any code, you must have an Editor role or higher on all account management services. To view or change roles, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).
{: tsResolve}
