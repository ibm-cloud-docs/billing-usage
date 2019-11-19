---

copyright:
  years: 2015, 2019
lastupdated: "2019-11-19"

keywords: promo code, feature code, Subscription account, Lite account, payment, invoice, credit card, subscription code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:support: data-reuse='support'}

# FAQs for billing and usage
{: #billusagefaqs}

FAQs for billing and usage might include questions about credit cards, promo codes, or subscriptions. To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](https://{DomainName}/docs/faqs).
{: shortdesc}

## What is a GB-hour?
{: #gb-hour}
{: faq}

Runtime and container usage is charged based on the following variables:
 * How much memory your runtime or container uses, in gigabytes (GB)
 * The duration that memory is used

Multiply the two values together, and the result is the GB-hour.

## What happens if my Lite plan instance reaches the monthly quota?
{: #monthlyquota}
{: faq}

When you reach any quota limit for Lite plan instances, the service for that month is suspended. Quota limits are per org and not per instance. New instances that are created in the same org show any usage from previous instances. The quota limits reset on the first of every month.

## How do I update my credit card?
{: #updatecard}
{: faq}
{: support}

Updating your credit card is just like adding a new one. Go to the [Payments](https://{DomainName}/billing/payments) page in the {{site.data.keyword.cloud_notm}} console, and in the Add Payment Method section, enter the billing information for your new card, then click **Add credit card**.

To switch to a different payment method, select **Pay with Other** and then click **Submit change request**. A support case to change your payment method will be created for you.

## Why won't my credit card go through?
{: #addcard}
{: faq}

Protecting your identity is a priority for us, so we take credit card verification seriously.

Contact us by calling 1-866-325-0045 and selecting the third option. Alternatively, you can email `verify@us.ibm.com` and include your IBMid and a copy of any error messages that displayed. Do not include any credit card information.

## What's the difference between promo codes and feature codes?
{: #promo-feature-codes}
{: faq}

Promo codes are for Pay-As-You-Go and Subscription accounts and give you limited-time credits toward your account and services. The codes are typically short phrases, like `PROMO200`. For more information about promo codes, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

Feature codes provide enhancements for Lite accounts, such as an unlimited number of organizations or converting a Lite account to a trial account. They're typically random alphanumeric codes, like `a1b2c3def456`. For more information about feature codes, see [Applying feature codes to Lite accounts](/docs/account?topic=account-codes).

## Where can I get a promo code?
{: #get-promo-code}
{:faq}

Promo codes are provided by {{site.data.keyword.Bluemix_notm}} sales on a limited basis. Promotions are meant for select groups and are typically given out at hackathons, conferences, and other events. 

## How do I apply a promo code?
{: #how-apply-promo}
{: faq}

To apply your promo code, go to the [Promotions](https://{DomainName}/billing/promotions) page in the console, enter your promo code, and click **Apply**. For more information, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

## How do I apply a feature code?
{: #entercode}
{: faq}
{: support}

Feature codes add extra capabilities to Lite accounts and are typically provided for educational initiatives or special events. To redeem your code, go to the [Account settings](https://{DomainName}/account/settings) page in the console, and click **Apply code**.

## Is there a monthly minimum amount required for Subscription accounts?
{: #subs-minimum}
{: faq}

Yes, your subscription must have a combined minimum spending and term commitment of $100.00 USD each month for 12 months.

## How do I add subscription credit to my account?
{: #subscriptioncode}
{: faq}
{: support}

After you purchase a subscription, you'll receive an email with a subscription code that adds the credit to your account. To apply the subscription code, go to [Account settings](https://{DomainName}/account/settings), and click **Apply code**. For more information, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions).

## Can I pay the total spending commitment up-front or quarterly?
{: #subs-pay-schedule}
{: faq}

Yes! By default, you're billed monthly for your subscriptions. If you'd like to pay up-front or quarterly, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg).

## Can I spend more or less than my monthly commitment?  
{: #subs-spending}
{: faq}

Yes, what you spend monthly is up to you! You can spend any amount of the total commitment each month.

## What happens if I spend my entire subscription amount before my term ends?  
{: #subs-spend-before-term-end}
{: faq}

You're required to continue paying your monthly charges until the end of your term. You're charged the non-discounted rate for any usage that goes over your total subscription amount. To avoid overage charges, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) to sign up for a new subscription.

## Can I cancel my Subscription account before the end of my term commitment?  
{: #subs-cancel-early}
{: faq}

A subscription is a contract between you and IBM that commits you to use {{site.data.keyword.Bluemix_notm}} for a specific term and spending amount. You can request to cancel your subscription before the end of the term, but whether the subscription can be canceled is at the discretion of IBM. Any remaining credit on your subscription might be forfeited. To inquire about this possibility, contact support. Make sure that you provide details about why you need to cancel your subscription.

## How can I monitor spending?
{: #monitor-spending}
{: faq}
You can view your monthly runtime and service usage by clicking **Manage > Billing and usage > Usage**. Learn more in [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## Can I receive notifications when my spending reaches specific levels?
{: #spending-notify}
{: faq}
{: support}

You can set separate spending thresholds for the account, container, runtime, all services, and specific services. You automatically receive notifications when your monthly spending reaches 80%, 90%, and 100% of those thresholds. To set spending notifications, click **Manage > Billing and usage** and select **Spending notifications**. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).

## Where can I access my invoice?
{: #access-invoices}
{: faq}
{: support}

If you have a billable account, you can access your invoice by clicking **Manage > Billing and usage**, and selecting **Invoices**. If you have a Lite account, you don't have an invoice because you're never charged for Lite plan usage.

For Pay-As-You-Go accounts that aren't billed in US dollars or Subscription accounts, you can also view your invoices on the [IBM Invoices website](https://www.ibm.com/invoices){: new_window} ![External link icon](../icons/launch-glyph.svg). See [How do I view invoices for Pay-As-You-Go or Subscription accounts?](/docs/billing-usage?topic=billing-usage-troubleshoot#ts_cant-view-invoice).

## Why does my usage not match my invoice?
{: #usage-not-match-invoice}
{: faq}
{: support}

Your usage might not match your invoice because the months that are used to compare usage aren't the same, or the total amount of the orgs wasn't selected. For more information, see [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage). If it still doesn't match, get in touch with us by calling 1-866-325-0045 and choosing the third option, or by opening a [support case](https://{DomainName}/unifiedsupport/supportcenter){: new_window} ![External link icon](../icons/launch-glyph.svg).

## Why can't I manage my invoices?
{: #slperm-manage-invoices}
{: faq}

The SoftLayer permission for managing invoices might not have been migrated correctly in {{site.data.keyword.Bluemix_notm}}. Ask your account owner to add you to the View account summary access group. For more information, see [Managing migrated SoftLayer account permissions](/docs/iam?topic=iam-migrated_permissions).

## How do I request paperless invoicing? 
{: #paperless-invoices}
{: faq}

To switch to paperless invoicing, you must submit a request to {{site.data.keyword.IBM_notm}} in writing through the {{site.data.keyword.IBM_notm}} Customer Support site. Paperless invoicing isn't available in all regions. 

1. Go to [{{site.data.keyword.IBM_notm}} Customer Support ![External link icon](../icons/launch-glyph.svg)](https://www.ibm.com/support/customer/zz/en/selectcountrylang.html){: new_window}, and select your region. 
2. Click **Contact us**. 
3. Click **Email us** in the Invoice, payment section.
4. Provide your {{site.data.keyword.IBM_notm}} customer number in your request to change to paperless billing. Click **Save**. If you don't know your customer number, contact {{site.data.keyword.Bluemix_notm}} Support by calling 1-866-325-0045 and selecting the third option or contact the [eCustomer Care team](https://www-112.ibm.com/software/howtobuy/passportadvantage/paocustomer/docs/en_US/ecare.html){:external} for help. 
5. Click **My Requests** to track the status your request.

## Does the price of the offering that I'm ordering reflect the discounted price?
{: #discount-price}
{: faq}

Yes, if your account includes any discounts, the price of the offering that is displayed in your infrastructure order summary does reflect the discounted price of that offering.

## How do I confirm that I received an expected credit?
{: #receive-credit}
{: faq}
{: support}

Credit might take a few hours to appear in your account.  To see whether a credit was added, go to **Manage > Billing and usage**, and select **Usage**. The credit might be listed in the Active subscriptions and credits section.

If the credit isn't on the Usage page, go to **Invoices** and click link with the date for your next recurring invoice. If you don't see the credit on the next recurring invoice, it is not yet added to your account. Check back later to verify that you received the credit.

## How do I get support?
{: #contactsupport}
{: faq}

Click **Support** in the console menu bar to access the Support Center. From there, start with leveraging the list of common FAQs. If you don't find the answers that you need, see the **Need more help?** section to contact IBM Cloud support.

## How do I cancel my account?
{: #cancelmyaccount}
{: faq}

We're sad to see you go! If there's any way we can assist you with your account before you go, reach out to us by contacting support.

If you do decide to leave, how you cancel your account depends on your account type. You can check your account type by going to [Account settings](https://cloud.ibm.com/account/settings) and looking under _Account Type_.

* For Pay-As-You-Go or Subscription accounts, the quickest way to cancel your account is to contact us through [live chat](https://{DomainName}/unifiedsupport/supportcenter) or by calling 1-866-325-0045 and selecting the third option. Alternatively, you can open a support case.
* To cancel a Lite account, go to [Account settings](https://{DomainName}/account/settings) and click **Deactivate account**.

## How do I delete my account?
{: #deleteaccount}
{: faq}

Contact [{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window} to open a support case and request to delete your account. If you have data that is associated with your old account that you want to move to a new account, include this information in your email.

Data in deleted accounts is not recoverable.

## Where can I view the billing address for my account? 
{: #billing-address}
{: faq}

You can view the primary contact and address that is associated with an account by going to **Manage** > **Account**, and selecting **Company profile**. 