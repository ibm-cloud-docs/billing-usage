---

copyright:
  years: 2017, 2020
lastupdated: "2020-04-10"

keywords: troubleshoot billing, billing error, payment error, feature code, subscription , cant add credit card, invoices, view invoice, subscription code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:tip: .tip}
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

  1. In the IBM Cloud console, go to **Manage > Access (IAM)**, and select **Users**.
  2. Click your name from the Users page.
  3. Click **Access policies** to view your assigned IAM access policies.
  4. If you don't have the required access, contact the account owner to request it.

For more information about account management services, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).

## Why can't I apply a subscription code?
{: #cannot-apply-subscription-code}
{: troubleshoot}

When you try to apply a subscription code, you see an error that states that the code cannot be applied.
{: tsSymptoms}

You might see this error if you don't have the required access in the account or the code expired.
{: tsCauses}

- Verify that you have access to apply the code. To apply any code, you must have an Editor role or higher on all account management services. To view or change roles, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).
- Contact the person who provided the code for help with reissuing an expired code.
{: tsResolve}

## How do I add a credit card when the option isn't available through the console?
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

  1. Go to [ibm.com](http://www.ibm.com){: external} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}.
  1. Click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg), and select **Billing**.
  1. Click **Manage payment method**.
  1. Enter your credit card information, and click **Register**.

The information is verified and added to your {{site.data.keyword.Bluemix_notm}} account as your payment method for any charges.

## Why can't I view the invoices for my Pay-As-You-Go or Subscription account in the console?
{: #ts_cant-view-invoice}
{: troubleshoot}

As a Pay-As-You-Go or Subscription account owner, you might not be able to view your invoices from the Invoices page in the {{site.data.keyword.Bluemix_notm}} console.

When you try to view your invoices, one of the following messages is displayed: 
{: tsSymptoms}

`Your invoices are managed through IBM.com.`

`This account is invoiced on a separate billing platform.`

If you have a Pay-As-You-Go account that is billed in a currency other than US dollars or a Subscription account, you view your invoices on the [IBM Invoices](http://ibm.com/invoices){: external} website, which is linked from the Invoices page in the console.
{: tsCauses}

If you're visiting the Invoices website for the first time, sign up with your IBMid and complete your profile. Then, add access to your account with your IBM customer number.
{: tsResolve}

1. Go to [IBM Invoices](http://ibm.com/invoices){: external}, and select your region.
1. Log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}. 
1. Complete your profile on the Invoices website. 
1. From the Invoices website, go to the Accesses tab. Add access to your account and provide your IBM customer number. If you don't know your customer number, contact IBM Cloud Support by calling 1-866-325-0045 and selecting the third option or contact the [eCustomer Care team](https://www-112.ibm.com/software/howtobuy/passportadvantage/paocustomer/docs/en_US/ecare.html){:external} for help. 


To access your invoices in the future, you can click the link from the Invoices page in the console or bookmark the external invoices website to go to it directly. For more information, see [Managing your invoices](/docs/billing-usage?topic=billing-usage-viewing-invoices).
{: tip}

## Why can't I apply a feature code?
{: #cannot-apply-feature-code}
{: troubleshoot}

When you try to apply a feature code, you see an error that states that the code cannot be applied.
{: tsSymptoms}

You might see this error for any of the following reasons:
{: tsCauses}

- Your account doesn't meet the requirements for the feature code.
- You don't have the required access in the account. 
- The code expired.


- Verify that you have the correct account type. For example, some feature codes for educational promotions are only for Lite accounts. To view your account type in the console, go to **Manage > Account**, and select **Account settings**. For more information, see [Applying feature codes](/docs/account?topic=account-codes).
- Verify that you have access to apply the code. To apply any code, you must have an Editor role or higher on all account management services. To view or change roles, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).
- Contact the person who provided the code for help with reissuing an expired code.
{: tsResolve}

## Why can’t I create a service after I apply a feature code?
{: #cant-create-service-feature-code}
{: troubleshoot}

When you try to create an instance of a service from the catalog, you're prompted to upgrade with a message such as `Upgrade your account to create instances of the offering.`
{: tsSymptoms}

Your account wasn't enabled to create resources of that type after you applied the feature code. The resources or capabilities that are provided vary for each feature code.
{: tsCauses}

Contact the person who gave you the feature code to verify the capabilities that it can enable for your account. For example, contact your educational provider for feature codes that they gave you for use with coursework.
{: tsResolve}
