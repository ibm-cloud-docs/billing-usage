---

copyright:
  years: 2015, 2023

lastupdated: "2023-06-28"


keywords: promo code, feature code, Subscription account, Lite account, payment, invoice, credit card, subscription code, paperless billing, billing item

subcollection: billing-usage

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQs for billing and usage
{: #billusagefaqs}

FAQs for billing and usage might include questions about credit cards, promo codes, or other billing-related issues. To find all FAQs for {{site.data.keyword.cloud}}, see our [FAQ library](/docs/faqs).
{: shortdesc}

## What is a GB-hour?
{: #gb-hour}
{: faq}

Runtime and container usage is charged based on the following variables:

* How much memory your runtime or container uses, in gigabytes (GB).
* The duration that memory is used.

Multiply the two values together, and the result is the GB-hour.

## How are bandwidth overage charges calculated for Bare Metal Servers and Virtual Servers?
{: #bandwidth-usage}
{: faq}

{{site.data.keyword.cloud_notm}} systems monitor all inbound and outbound traffic for a server regardless of the type of traffic. Based on the allocated bandwidth for a server, overages are assessed for excess traffic, which is monitored at the network switch level. Monitor your bandwidth usage with bandwidth graphs. For information, see [Viewing bandwidth graphs](/docs/bare-metal?topic=bare-metal-bm-view-bandwidth-graphs).


## How do I prevent bandwidth overages?
{: #bandwidth-usage-overages}
{: faq}

If you provision multiple servers, you can potentially reduce future bandwidth overage charges by pooling your servers' bandwidth. For more information, see [Optimizing your bandwidth usage](/docs/bare-metal?topic=bare-metal-bm-view-bandwidth-graphs#bm-optimize-bandwidth-usage). Contact an [{{site.data.keyword.cloud_notm}} Sales](/catalog?contactmodule){: external} representative to request a quote for additional server bandwidth.

##  What's the difference between a Pay-As-You-Go and Subscription account?
{: #billable-account-types}
{: faq}

With Pay-As-You-Go accounts, you're billed monthly for your resource usage. Your resource usage consists of recurring and fluctuating costs. This account type is a good fit for developers or companies that want to explore the entire {{site.data.keyword.cloud_notm}} catalog but have smaller or variable workloads. You pay only for what you use or commit to on a monthly basis, with no long-term contracts. Usage consists of products, services, and resources.

With Subscription accounts, you buy a subscription for an amount of credit to spend on resource usage within a certain time period. In exchange for this spending commitment, you get a discount on your usage costs. For more information about the differences between account types, see [Account types](/docs/account?topic=account-accounts).

## What happens if my Lite plan instance reaches the monthly quota?
{: #monthlyquota}
{: faq}
{: support}

When you reach any quota for Lite plan instances, the service for that month is suspended. Quotas are based per org and not per instance. New instances that are created in the same org show any usage from previous instances. The quota resets on the first of every month.

## Can I use PayPal as a payment method?
{: #paypal}
{: faq}
{: support}

As of March 31, 2023, PayPal is no longer accepted.

## Can I update my credit card?
{: #updatecard}
{: faq}
{: support}

Updating your credit card is just like adding a new one. Go to the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console. In the Add Payment Method section, enter the billing information for your new card, and click **Add credit card**.

To switch to a different payment method, select **Pay with Other**, and click **Submit change request**. A support case to change your payment method is then created for you.

If your payments are managed outside of the console, go to IBM.com and log in to the Manage Payment Method application to update your credit card. For more information, see [How do I add a credit card when the option isn't available through the console?](/docs/billing-usage?topic=billing-usage-ts-ccibm)

## How do I change my payment method?
{: #pay-method}
{: faq}

For a Pay-As-You-Go account, you must have an active credit card on file. Our Subscription and {{site.data.keyword.cloud_notm}} Enterprise Savings Plan account types might enable you to use other payment options. Contact an [{{site.data.keyword.cloud_notm}} Sales](/catalog?contactmodule){: external} representative to inquire about payment options.

## Why didn't my credit card process?
{: #addcard}
{: faq}

Protecting your identity is a priority for us, so we take credit card verification seriously.

If your credit card did not process successfully, contact us by calling 1-866-325-0045 and selecting the third option. For information about specific error messages, see [Credit Card error messages](/docs/billing-usage?topic=billing-usage-cc-error-messages).

You might manage your payment method on a separate billing platform, [{{site.data.keyword.IBM_notm}} Billing](https://myibm.ibm.com/billing/). For more information about that process, see [Managing your payment method outside of the console](/docs/billing-usage?topic=billing-usage-linkedusage#payment-method-ibm).

## Can I check the status of my account's updated payment method?
{: #payment-method-status}
{: faq}

Yes, you can. When you request to change your payment method, a support case is created automatically. Go to the [Manage cases](/unifiedsupport/cases) page in the {{site.data.keyword.cloud_notm}} console to view the status of your request.

## Can I delete my credit card?
{: #removecard}
{: faq}

For Pay-As-you-Go accounts, you must have an active credit card on file. You can replace an existing credit card with a new one.

* If you're using a new US-based Pay-As-You-Go account with credit card billing, you can add a new credit card in the Monthly Payment Method form on the [Payments](/billing/payments){: external} page.
* For all other accounts, you can remove a credit card and switch to a different payment method by clicking **Pay with Other** > **Submit change request**. To complete the change, review and update the support case that is created for you.
* If you manage your payment method on a separate billing platform, you can remove your credit card by going to [{{site.data.keyword.IBM_notm}} Billing](https://myibm.ibm.com/billing/){: external}. For more information, see [Managing your payment method outside of the console](/docs/billing-usage?topic=billing-usage-linkedusage#payment-method-ibm).

## How do I change the invoice currency from US Dollars to my local currency?
{: #localcurrency}
{: faq}

Invoicing in your local currency might be possible if you have a subscription or {{site.data.keyword.Bluemix_notm}} Cloud Enterprise Savings Plan account type. Contact [{{site.data.keyword.Bluemix_notm}} Cloud Sales](/catalog?contactmodule){: external} for more information.

An account that is invoiced in a currency other than US Dollars can't be converted to US Dollar invoicing.
{: note}

## What is Business Continuity Insurance?
{: #BCI-invoice}
{: faq}

Business Continuity Insurance is insurance that protects you from illegitimate charges against your servers. You can request this insurance through [{{site.data.keyword.Bluemix_notm}} Cloud Sales](/catalog?contactmodule){: external} to avoid overage charges if a documented network attack occurs against a covered server. {{site.data.keyword.Bluemix_notm}} credits back any overages incurred on the affected server.

To receive the credits for illegitimate charges against your servers, contact [{{site.data.keyword.Bluemix_notm}} Support](/unifiedsupport/supportcenter){: external} and open a support case.


## What is the `Service: Support and Services` charge on my invoice?
{: #supserve-invoice}
{: faq}

If you create a VMWare cluster on your {{site.data.keyword.Bluemix_notm}} account, you are charged for VMWare Level 2 Support for each cluster instance. This charge is in addition to any {{site.data.keyword.Bluemix_notm}} Support charges for Premium or Advanced Support.

## What's the difference between promo codes and feature codes?
{: #promo-feature-codes}
{: faq}

Promo codes are for Pay-As-You-Go and Subscription accounts and give you limited-time credits toward your account and {{site.data.keyword.Bluemix_notm}} products. The codes are typically short phrases, like `PROMO200`. For more information about promo codes, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

Feature codes provide enhancements for an account, such as an unlimited number of organizations or creating a trial account. Feature codes are typically provided for online courses and certain events, such as educational sessions or conference workshops. They're typically random alphanumeric codes, like `a1b2c3def456`. For more information about feature codes, see [Applying feature codes](/docs/account?topic=account-codes).

## Where can I get a promo code?
{: #get-promo-code}
{: faq}

Promo codes are provided on a limited basis by {{site.data.keyword.Bluemix_notm}} sales to customers with Pay-As-You-Go and Subscription accounts. Promotions provide specific discounts for a set amount of time. For more information, see [Applying promo codes](/docs/account?topic=billing-usage-applying-promo-codes).

## Where can I get a feature code?
{: #get-feature-code}
{: faq}

Feature codes are provided by {{site.data.keyword.Bluemix_notm}} sales and educational providers on a limited basis. Feature codes are meant for select groups and are typically given out at hackathons, conferences, and other events. If you are taking a course through an educational provider and need additional resources to complete the course, contact your educational provider to determine if a feature code is applicable.

## How do I apply a promo code?
{: #how-apply-promo}
{: faq}

To apply your promo code, go to the [Promotions](/billing/promotions) page in the console, enter your promo code, and click **Apply**. For more information, see [Applying promo codes](/docs/billing-usage?topic=billing-usage-applying-promo-codes).

You might be looking for information on feature codes and subscription codes. For more information, see [Applying feature codes](/docs/account?topic=account-codes) and [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code).

If you can't apply a promo code that you received from {{site.data.keyword.Bluemix_notm}} Sales or an educational provider, contact sales or the provider for additional help.
{: note}

## Why did I get invoiced when I have remaining promotion credits?
{: #billed-promo}
{: faq}

If you think your invoice didn't include your promotion credits, first determine that the credits are still active on your account by using the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Billing and usage**, and select **Promotions and credits**.
1. Click a promotion to expand the table and view the amount of each promotion, the duration of each promotion and the product it applies to.
1. Check the following to make sure that your promo code is still applicable:
   - Verify the maximum value of the promo code per month. Some monthly recurring promo codes have a monthly limit. If your usage exceeded that limit, you're billed for the remaining amount.
   - Compare the date of your invoice to the start and end dates of the promo code. If you applied the promo code after the invoice was issued, it was not applied to that month's invoice.
   - If you didn't use the products that are impacted by the promo code before it expired, you don't receive the promotion credits.

After you complete these steps, if you still believe that the invoice amount is an error, create a support case. Go to the [Support Center](/unifiedsupport/supportcenter) and click **Create a case**.


## How do I apply a feature code?
{: #entercode}
{: faq}
{: support}

Feature codes add extra capabilities in an account and are typically provided for educational initiatives or special events. To redeem your code, go to the [Account settings](/account/settings) page in the console, and click **Apply code**. You can also apply your code to a new account by clicking **Register with a code** when you [sign up for a new account](/registration).

You might be looking for information about promo codes and subscription codes, which are available for certain account types. For more information, see [Managing promotions](/docs/billing-usage?topic=billing-usage-applying-promo-codes) and [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code).


## Why did my account get billed for additional services charges?
{: #getting-billed}
{: faq}

As the account owner, you're responsible for all charges that are incurred by users in your account, including invited users. Ensure that each user is assigned only the level of access that is required to complete their job, including the ability to create new instances that might incur extra charges in your account. For more information, see [Managing access to resources](/docs/account?topic=account-assign-access-resources).

Resources and applications that are left running in an account are subject to charges based on the pricing and description of the product. For example, this includes buildpacks, Platform as a Service, and Infrastructure as a Service.

If you believe that charges on your invoice are incorrect, [contact Support](/unifiedsupport/supportcenter){: external} within 30 calendar days of the invoice due date or use the contact information that is found on your invoice.


## Why did I get billed for a resource I deleted?
{: #stop-billing}
{: faq}

A [resource](#x2004267){: term} is anything that you can create from the catalog that is managed by and contained within a resource group. You're billed for resources in your account until you cancel them. If you deleted a resource or have resources in your account that are no longer used, make sure to cancel all billing items associated with those resources. Billing items can't be recovered after they are canceled. For more information, see [Cancelling your billing items](/docs/billing-usage?topic=billing-usage-cancel-billing-items).


## Can I add a tax identification number to my account?
{: #tax-assessment}
{: faq}

If you are not subject to tax, you can provide us with a tax identification number by using the contact information that is found on your most recent invoice. After your tax identification number is accepted, you are not charged taxes on any future invoices. The removal of tax charges from your account is not retroactive and can't be refunded.

{{site.data.keyword.cloud_notm}} complies with all tax regulations. Taxes are assessed based on the laws that correspond to the address on your account.
{: note}

## How can I monitor spending?
{: #monitor-spending}
{: faq}

You can view your monthly runtime and service usage by clicking **Manage > Billing and usage > Usage**. Learn more in [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## Can I receive notifications when my spending reaches specific levels?
{: #spending-notification}
{: faq}
{: support}

You can set separate spending thresholds for the account, container, runtime, all services, and specific services. You automatically receive notifications when your monthly spending reaches 80%, 90%, and 100% of those thresholds. To set spending notifications, click **Manage > Billing and usage** and select **Spending notifications**. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).

Spending notifications don't stop charges from incurring. You continue to incur charges if your usage exceeds 100% of the spending threshold.
{: note}

## Does the price of the product that I'm ordering reflect the discounted price?
{: #discount-price}
{: faq}

Yes, if your account includes any discounts, the price of the product that is displayed in your infrastructure order summary does reflect the discounted price of that product.

## How do I confirm that I received an expected credit?
{: #receive-credit}
{: faq}
{: support}

Credit might take a few hours to appear in your account. To see whether a credit was added, go to **Manage > Billing and usage**, and select **Usage**. The credit might be listed in the Active subscriptions and credits section.

If the credit isn't on the Usage page, go to **Invoices** and click link with the date for your next recurring invoice. If you don't see the credit on the next recurring invoice, it is not yet added to your account. Check back later to verify that you received the credit.

## How do I get answers to my Startup with IBM questions?
{: #startup-ibm}
{: faq}

Startup with IBM Program, which was formerly the IBM Global Entrepreneur Program (GEP), is available by going to the [Startup with IBM Program](https://developer.ibm.com/startups/){: external}. The awarding and extension of credits through this IBM corporate program isn't directly supported by {{site.data.keyword.cloud_notm}} Support. If your application to the program is approved, credits might be referred to as the Technology Incubator Program on an {{site.data.keyword.cloud_notm}} Invoice. For more information about the program and its credits, visit the [Frequently Asked Questions for the Startup with IBM Program](https://developer.ibm.com/startups/faq){: external}.

## Where can I find my credits for {{site.data.keyword.IBM_notm}} corporate programs?
{: #ibm-corporate-credits}
{: faq}

Credits for {{site.data.keyword.IBM_notm}} corporate programs, such as Startup with {{site.data.keyword.IBM_notm}} and PartnerWorld, are available within the applicable invoice in {{site.data.keyword.Bluemix_notm}}. To view the credits, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Invoices**.
1. Select an applicable invoice.
1. Find the name of the program listed in the Current Payment Method section to see the monthly credit, applied credit, and remaining credit information.


## How do I get support?
{: #contactsupport}
{: faq}

Go to the [Support Center](/unifiedsupport/supportcenter){: external} page by clicking the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center** from the console menu bar. From there, review the list of common FAQs. If you don't find the answers that you need, review the **Contact Support** section. For more information on account types and support products, see [Basic, Advanced, and Premium Support plans](/docs/get-support?topic=get-support-support-plans).

## Where can I view the billing address for my account?
{: #billing-address}
{: faq}

You can view the primary contact and address that is associated with an account by going to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and selecting **Company profile**.

## How can I ensure that my account is secure to avoid charges due to unauthorized access?
{: #unauth-charges}
{: faq}

As a self-managed platform, the security of an account is the responsibility of the account owner and all users with access to the account. Any charges that result from unauthorized access are the responsibility of the account owner.

To prevent unauthorized access, change your password regularly and require the use of multifactor authentication by all users on your account. These options include the use of time-based one-time passcode authentication, security questions, third-party authentication mechanisms, and password expiration rules. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).

You can regularly review the list of account users and remove users who don't need access to the account. For more information, see [Removing users from an account](/docs/account?topic=account-remove).
{: tip}
