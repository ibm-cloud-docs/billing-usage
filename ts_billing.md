---

copyright:
  years: 2017, 2019
lastupdated: "2019-09-19"

keywords: troubleshoot billing, billing error, payment error, feature code, subscription , cant add credit card

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


## How do I add a credit card when the option is unavailable through the console?
{: #ts_ccibm}
{: troubleshoot}

You want to enter a credit card to pay for {{site.data.keyword.Bluemix_notm}} services, but the option doesn't appear.

When you try to enter your credit card information, you see the following message:
{: tsSymptoms}

`Your payments are managed through IBM.com. To view your payments and maintain your billing, you can visit the IBM.com portal which contains everything for your IBMid account.`

You click **Explore** to access the ibm.com website, but you don't see a location to enter your credit card information.

Credit card transactions are securely processed through the {{site.data.keyword.Bluemix_notm}} console. However, in some countries, extra steps are taken to ensure the integrity of the credit card data. Those credit card requests are completed through the ibm.com website. Both methods ensure that your credit card information is securely processed.   
{: tsCauses}

To provide your credit card information for payment, complete the following steps:
{: tsResolve}

  1. Go to [ibm.com ![External link icon](../icons/launch-glyph.svg "External link icon")](http://www.ibm.com){: new_window} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}.
  1. Click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg), and select **Billing**.
  1. Click **Manage payment method**.
  1. Enter your credit card information, and click **Register**.

The information is verified and added to your {{site.data.keyword.Bluemix_notm}} account as your payment method for any charges.

