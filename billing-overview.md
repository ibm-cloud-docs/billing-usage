---

copyright:
  years: 2019, 2024
lastupdated: "2024-04-01"

keywords: IBM Cloud billing, payments, costs, usage, spending

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Video - How can I manage billing and usage in {{site.data.keyword.cloud_notm}}?
{: #overview}

Learn about the {{site.data.keyword.cloud}} billing options and tools that you can use to track your usage and manage invoicing and payments.
{: shortdesc}

![Introduction to IBM Cloud billing and usage](https://www.kaltura.com/p/1773841/sp/177384100/embedIframeJs/uiconf_id/27941801/partner_id/1773841?iframeembed=true&entry_id=1_w31ph24n){: video output="iframe" data-script="#video-transcript-billing-usage" id="mediacenter-player" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen}

## Video transcript
{: #video-transcript-billing-usage}
{: notoc}

{{site.data.keyword.cloud_notm}} offers multiple billing options so you can tailor how you pay based on your resource usage and your organization's procurement practices. You get the most flexibility with a Pay-As-You-Go account. You pay only for the billable services that you use each month, with no long-term contracts or commitments. If you know you have a significant amount of usage, you can purchase a subscription to get a discount. With a subscription, you commit to a certain amount of usage over a period of time. The larger the subscription, the better the discount. You can choose to pay upfront or be billed monthly, quarterly, or annually.

As an account owner, you have full access to monitoring resource usage, viewing invoices, and managing payments in the console. However, if you want to delegate billing tasks to another user, you can assign a user an Identity and Access Management (IAM) policy with the Administrator role on the Billing account management service.

When you're ready to start tracking your resource usage and managing your billing and payment preferences, go to the Billing and usage section of the {{site.data.keyword.cloud_notm}} console. Monitoring resource usage can help you understand what's coming in your next bill. On the Usage page, you can view current and past usage, and drill down by resource type to view the plans and instances in your account.

You can also export usage reports and choose from a high-level summary overview or a service instance view. If you use tags to organize your resources such as by team or cost center, you can sort your instance report by the tags to identify the associated usage.

Setting spending limits is another helpful way to keep an eye on usage in your account. You can set notifications for total account, runtime, container, and service spending. When you reach a percentage of the spending limit that you set, you are notified immediately by email.

To view your current balance, manage your payment method, or make a one-time payment, go to the Payments page. You can download your latest invoice with all discounts and charges here or from the Invoices page. 

Now that you've walked through the common billing options and how to delegate billing administrator capabilities, track usage, and pay your bill, you're ready to start deciding what is best for your account. As always, if you need more information, check out the documentation for {{site.data.keyword.cloud_notm}} billing and usage.

## How does billing work in {{site.data.keyword.cloud_notm}}?
{: #how-billing-works}

{{site.data.keyword.cloud_notm}} has two billable account types, Pay-As-You-Go and Subscription accounts. With a billable account, you can use {{site.data.keyword.cloud_notm}} resources and services that incur costs. The account type that you choose impacts how you're billed for your resource usage.

When you have a Pay-As-You-Go account, you're billed monthly for your resource usage. You pay only for what you use, with no long-term contracts. As your resource usage changes, so does your invoice, similar to a utility bill. This account type is a good fit for developers or companies that want to explore the entire {{site.data.keyword.cloud_notm}} catalog but have smaller or variable workloads.

When you have a Subscription account, you buy a subscription for an amount of credit to spend on resource usage within a certain time period. In exchange for this spending commitment, you get a discount on your usage costs. For example, you might buy a subscription for $12,000 USD a year that comes with a 10% discount. No matter when you incur usage costs within that year, you get fixed billing for the subscription amount, such as $1,000 a month. This account type is a good fit for enterprise organizations with large cloud workloads that want the predictability of fixed billing for their financial planning.

In addition to the two billable account types, customers that have a Subscription account can sign up for the Enterprise Savings Plan billing model. This billing model is similar to a Subscription account with a few added benefits. The following table details the two billable account types and billing model.

| Pay-As-You-Go | Subscription| Enterprise Savings Plan|
|----------|---------|---------|
| Monthly billing | Timely billing | Timely billing |
| Invoiced on monthly consumption	| Invoices independent of usage | Invoiced on monthly consumption	|
| Best suited for developers and companies	| Best suited for enterprise organizations| Best suited for both developers and enterprise organizations|
{: caption="Table 1. Comparative analysis of account types" caption-side="bottom"}

### Estimating your costs
{: #charges-cost-estimation}

After you select the type of account that fits your organization's needs, it's time to understand how you will be charged for it. With an {{site.data.keyword.cloud_notm}} billable account, you're charged for the compute, containers, and services that your organization consumes. You might be invited by other {{site.data.keyword.cloud_notm}} users to participate in organizations under a different account. The usage for the apps or services that you use in the organizations that you're invited to are charged to the account that contains those organizations.

The following are the various charging types:
* **Fixed:** Fixed-rate pricing is based on an agreed upon monthly charge that isn't adjusted.
* **Metered:** Metered-usage pricing is based on the number of GB hours that are consumed for runtimes and the number of IP addresses and storage for containers.
* **Tiered:** Some pricing plans are based on a tiered pricing model, so you can get a volume-based discount according to your actual usage. Services might offer simple, graduated, or block tier pricing plans.
* **Reserved:** Reserved pricing is based on a long-term commitment for a service, so you can get a discounted price. With a reserved plan, you get a dedicated service instance that is easy to set up, deploy, and deliver in the public {{site.data.keyword.cloud_notm}} environment.

### Managing your payments
{: #payments}

If you're a new Pay-As-You-Go account owner that is located in the US and you are paying with a credit card, you can replace your current card with a new one or edit the details of an existing card. In either case, you manage your credit card from the [Payments](/billing/payments) page in the {{site.data.keyword.cloud_notm}} console.

If you own one of the following accounts, in the {{site.data.keyword.cloud}} console, you can go to **Manage** > **Billing and usage** to make a one-time payment, change your credit card details, view your billing items, and manage your invoices.
* New and existing Pay-As-You-Go accounts based in the US with any payment method other than a credit card
* New and existing Pay-As-You-Go accounts not based in the US
* New and existing Subscription accounts worldwide

 The process for updating a credit card requires a manual review that might take a few days to process. To view your open change request cases, go to [{{site.data.keyword.cloud_notm}} Support](https://cloud.ibm.com/unifiedsupport/supportcenter).
{: tip}

You might manage your payment method on a separate billing platform. You can easily register, update, or delete a payment method by going to [IBM Billing](https://myibm.ibm.com/billing/).

For more information about how to manage your payments, see [Managing your payment method](/docs/billing-usage?topic=billing-usage-linkedusage#prereqs-payments).

### Tracking your usage
{: #tracking-usage}

To view usage data for resources, you must be assigned the correct access. Access can be assigned at the account level or to individual resource groups.

* To view usage for all resources in the account, you need an access policy with the Administrator role on the Billing account management service.
* To view usage only for specific {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) resources, you need the Viewer role or higher on the resource group.

You can limit the access to view the usage for a specific resource group by assigning the viewer role or higher on all Identity and Access enabled services within that resource group.

### Managing your invoices
{: #view-manage-invoice}

If you have a Pay-As-You-Go account that's billed in US dollars, you can view your invoice in the {{site.data.keyword.cloud_notm}} console by going to **Manage** > **Billing and usage**, > and clicking **Invoices**.

If you own one of the following accounts, you can view your invoice on the [{{site.data.keyword.IBM_notm}} Invoices](https://www.ibm.com/support/customer/invoices/){: external} website, which is linked from the [Invoices page](/billing/invoices) in the console.

* New and existing Pay-As-You-Go accounts based in the US with any payment method other than a credit card
* New and existing Pay-As-You-Go accounts not based in the US
* New and existing Subscription accounts worldwide

New {{site.data.keyword.cloud_notm}} Pay-As-You-Go accounts for US customers with credit card billing can now view all classic infrastructure and platform services on one invoice. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Invoices**.
{: note}

For more information about invoices, see [Managing your invoices](/docs/billing-usage?topic=billing-usage-managing-invoices).

### Enterprise Savings Plan billing model
{: #commitment-model}

{{site.data.keyword.cloud_notm}} customers with a Subscription account can sign up for the Enterprise Savings Plan billing model. With this billing model, you commit to spend a certain amount on {{site.data.keyword.Bluemix_notm}} and you receive discounts across the platform. You are billed monthly based on your usage and you continue to receive a discount even after you reach your committed amount. For more information about the billing model, see [Enterprise Savings Plan billing model](/docs/billing-usage?topic=billing-usage-committed-use).

Premium and advanced support options are available for Enterprise Savings Plan. Support plan pricing falls into two tiers depending on the price level of your commitment. For more information, see [Support options for Enterprise Savings Plan](/docs/get-support?topic=get-support-support-plans#support-plans).
