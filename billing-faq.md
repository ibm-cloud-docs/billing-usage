---

copyright:
  years: 2015, 2021
lastupdated: "2021-06-10"

keywords: promo code, feature code, Subscription account, Lite account, payment, invoice, credit card, subscription code, paperless billing, billing item 

subcollection: billing-usage

content-type: faq

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:external: target="_blank" .external}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}
{:note: .note}

# FAQs for billing and usage
{: #billusagefaqs}

FAQs for billing and usage might include questions about credit cards, promo codes, or other billing-related issues. To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](https://{DomainName}/docs/faqs).
{: shortdesc}

## What is a GB-hour?
{: #gb-hour}
{: faq}

Runtime and container usage is charged based on the following variables:
 * How much memory your runtime or container uses, in gigabytes (GB).
 * The duration that memory is used.

Multiply the two values together, and the result is the GB-hour.

## What happens if my Lite plan instance reaches the monthly quota?
{: #monthlyquota}
{: faq}

When you reach any quota for Lite plan instances, the service for that month is suspended. Quotas are based per org and not per instance. New instances that are created in the same org show any usage from previous instances. The quota resets on the first of every month.

## Can I update my credit card?
{: #updatecard}
{: faq}
{: support}

Updating your credit card is just like adding a new one. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.

To switch to a different payment method, select **Pay with Other**, and click **Submit change request**. A support case to change your payment method is then created for you. 

If your payments are managed outside of the console, go to IBM.com and log in to the Manage Payment Method application to update your credit card. For more information, see [How do I add a credit card when the option isn't available through the console?](/docs/billing-usage?topic=billing-usage-ts_ccibm).

Some payment methods, such as PayPal, aren't accepted as recurring payment methods. You must manually submit the payment each month.
{: note}

## Why won't my credit card go through?
{: #addcard}
{: faq}

Protecting your identity is a priority for us, so we take credit card verification seriously.

Contact us by calling 1-866-325-0045 and selecting the third option. Alternatively, you can email `verify@us.ibm.com` and include your IBMid and a copy of any error messages that displayed. Don’t include any credit card information.

You might manage your payment method on a separate billing platform. You can easily register, update, or delete a payment method by going to [IBM Billing](https://myibm.ibm.com/billing/). For more information, see [Managing your payment method outside of the console](/docs/billing-usage?topic=billing-usage-linkedusage#payment-method-ibm).

For additional information about specific error messages, see [Why can't I upgrade my IBM Cloud account?](/docs/account?topic=account-ts_upgrade_cc).

## Can I delete my credit card?
{: #removecard}
{:faq}

You must have an active credit card or PayPal account on file. You can replace an existing credit card with a new one. 

* If you're using a new US-based Pay-As-You-Go account with credit card billing, you can replace your credit card by going to the [Support Center](https://{DomainName}/unifiedsupport/supportcenter){: external} and opening a support case. 
* For all other accounts, you can remove a credit card and switch to a different payment method by clicking **Pay with Other** > **Submit change request**. To complete the change, review and update the support case that is created for you.
* If you manage your payment method on a separate billing platform, you can remove your credit card by going to [{{site.data.keyword.IBM_notm}} Billing](https://myibm.ibm.com/billing/){: external}. 

## What's the difference between promo codes and feature codes?
{: #promo-feature-codes}
{: faq}

Promo codes are for Pay-As-You-Go and Subscription accounts and give you limited-time credits toward your account and services. The codes are typically short phrases, like `PROMO200`. For more information about promo codes, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

Feature codes provide enhancements for Lite accounts, such as an unlimited number of organizations or converting a Lite account to a trial account. They're typically random alphanumeric codes, like `a1b2c3def456`. For more information about feature codes, see [Applying feature codes to Lite accounts](/docs/account?topic=account-codes).

## Where can I get a promo code?
{: #get-promo-code}
{:faq}

Promo codes are provided by {{site.data.keyword.Bluemix_notm}} sales and educational providers on a limited basis. Promotions are meant for select groups and are typically given out at hackathons, conferences, and other events.

You might be looking for information on feature codes and subscription codes, which are available for certain account types. For more information, see [Applying feature codes to Lite accounts](/docs/billing-usage?topic=account-codes) and [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code). 

## How do I apply a promo code?
{: #how-apply-promo}
{: faq}

To apply your promo code, go to the [Promotions](https://{DomainName}/billing/promotions) page in the console, enter your promo code, and click **Apply**. For more information, see [Applying promo codes](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

You might be looking for information on feature codes and subscription codes, which are available for certain account types. For more information, see [Applying feature codes to Lite accounts](/docs/billing-usage?topic=account-codes) and [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code). 

## Why did I get billed if I have remaining promotion credits?
{: #billed-promo}
{: faq}

If you think your invoice didn't include your promotion credits, first determine that the credits are still active on your account by using the following steps: 

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Billing and usage**, and select **Promotions**.  
1. Click a promotion to expand the table and view a description of each promotion and the offerings it applies to.
1. Check the following to make sure that your promo code is still applicable:
  - Verify the maximum value of the promo code per month. Some monthly recurring promo codes have a monthly limit. If your usage exceeded that limit, you're billed for the remaining amount.  
  - Compare the date of your invoice to the start and end dates of the promo code. If you applied the promo code after the invoice was issued, it was not applied to that month's invoice. 
  - If you didn't use the products that are impacted by the promo code before it expired, you don't receive the promotion credits.
  
After you complete these steps, if you still believe that the invoice amount is an error, create a support case. Go to the [Support Center](https://{Domain}/unifiedsupport/supportcenter) and click **Create a case**. 

## How do I apply a feature code?
{: #entercode}
{: faq}
{: support}

Feature codes add extra capabilities to Lite accounts and are typically provided for educational initiatives or special events. To redeem your code, go to the [Account settings](https://{DomainName}/account/settings) page in the console, and click **Apply code**.

You might be looking for information about promo codes and subscription codes, which are available for certain account types. For more information, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes) and [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code). 

## How can I monitor spending?
{: #monitor-spending}
{: faq}
You can view your monthly runtime and service usage by clicking **Manage > Billing and usage > Usage**. Learn more in [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## Can I receive notifications when my spending reaches specific levels?
{: #spending-notify}
{: faq}
{: support}

You can set separate spending thresholds for the account, container, runtime, all services, and specific services. You automatically receive notifications when your monthly spending reaches 80%, 90%, and 100% of those thresholds. To set spending notifications, click **Manage > Billing and usage** and select **Spending notifications**. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).

Your account is charged if your usage exceeds 100% of the spending threshold. 
{: note} 

## Does the price of the offering that I'm ordering reflect the discounted price?
{: #discount-price}
{: faq}

Yes, if your account includes any discounts, the price of the offering that is displayed in your infrastructure order summary does reflect the discounted price of that offering.

## How do I confirm that I received an expected credit?
{: #receive-credit}
{: faq}
{: support}

Credit might take a few hours to appear in your account. To see whether a credit was added, go to **Manage > Billing and usage**, and select **Usage**. The credit might be listed in the Active subscriptions and credits section.

If the credit isn't on the Usage page, go to **Invoices** and click link with the date for your next recurring invoice. If you don't see the credit on the next recurring invoice, it’s not yet added to your account. Check back later to verify that you received the credit.

## How can I add funds to my ResellOne account?
{: #resell}
{: faq}

If you have a separate ResellOne account with IBM, you can add funds through {{site.data.keyword.cloud_notm}}. To add funds to your ResellOne account, you must make a one-time payment by going to the [Manual payments](https://{DomainName}/billing/payments/manualpayment){: external} page in the {{site.data.keyword.cloud_notm}} console.

This amount must include any applicable tax. 
{: note}

After you submit the payment, contact the [Support Center](https://{DomainName}/unifiedsupport/supportcenter){: external} to request that the funds are applied to your ResellOne Account. You must submit the name of the ResellOne account and the amount before any applicable tax to {{site.data.keyword.cloud_notm}} Support. 

## How do I get answers to my Startup with IBM questions?
{: #startup-ibm}
{: faq}

Startup with IBM Program, which was formerly the IBM Global Entrepreneur Program (GEP), is available by going to the [Startup with IBM Program](https://developer.ibm.com/startups/){: external}. The awarding and extension of credits through this IBM corporate program isn'te directly supported by IBM Cloud Support. If your application to the program is approved, credits might be referred to as the Technology Incubator Program on an IBM Cloud Invoice. For more information about the program and its credits, visit the [Frequently Asked Questions for the Startup with IBM Program](https://developer.ibm.com/startups/faq){: external}.

## How do I get support?
{: #contactsupport}
{: faq}

Go to the [Support Center](https://{DomainName}/unifiedsupport/supportcenter){: external} page by clicking **Support** on the {{site.data.keyword.cloud}} console header. From there, review the list of common FAQs. If you don't find the answers that you need, see the **Contact Support** section to contact IBM Cloud Support. For more information on account types and support offerings, see [Basic, Advanced, and Premium Support plans](/docs/get-support?topic=get-support-support-plans).

## Where can I view the billing address for my account? 
{: #billing-address}
{: faq}

You can view the primary contact and address that is associated with an account by going to **Manage** > **Account**, and selecting **Company profile**. 
