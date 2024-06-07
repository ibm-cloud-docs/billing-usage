---

copyright:
  years: 2020, 2024
lastupdated: "2024-06-07"

keywords: troubleshoot billing, billing error, billing info, can't access billing, function unavailable

subcollection: billing-usage

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I access billing information?
{: #cannot-access-billing-info}
{: troubleshoot}

You must have the correct authorization on the account to view billing information.
{: shortdesc}

When you try to access your billing information, such as payments and invoices, you get a message that says the function isn't available.
{: tsSymptoms}

You see the following message because you don't have authorization to view the billing information for the account.
{: tsCauses}

> To manage invoices and payments, you need an IAM access policy with the Operator role or higher on the Billing account management service. To view usage information for the entire account, you need the Administrator role on the Billing service. Account owners can always view billing information for the account.

Check your access by completing the following steps:
{: tsResolve}

1. In the {{site.data.keyword.Bluemix}} console, go to **Manage, > Access (IAM)**, and select **Users**.
2. Click your name from the Users page.
3. Click **Access policies** to view your assigned IAM access policies.
4. If you don't have the required access, contact the account owner to request it.

For more information about account management services, see [Assigning access to account management services](/docs/account?topic=account-account-services).
