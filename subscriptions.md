---

copyright:
  years: 2019
lastupdated: "2019-09-23"

keywords: subscription, credit, subscription code, support code, subscription overage, subscription usage, feature code

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:important: .important}
{:screen: .screen}
{:new_window: target="_blank"}
{:note: .note}

# Managing subscriptions
{: #subscriptions}

With an {{site.data.keyword.cloud}} subscription, you get discounted usage for platform services and support by committing to a minimum spending commitment for a certain period of time. You can buy your first subscription, add more subscriptions, and monitor subscription usage on the Subscriptions page in the console.
{: shortdesc}

If you buy a subscription, your account is converted to a Subscription account type. Learn more about other benefits of Subscription accounts in [Account types](/docs/account?topic=account-accounts).
{: tip}

## How subscription credit is spent
{: #subscription-basics}

Subscriptions can provide the following two types of credit, which are divided into separate pools:
* Credit from platform subscriptions that pays for resource usage
* Credit from support subscriptions that pays for support costs

Each platform or support subscription is purchased for a given credit amount and duration. If the subscription duration is more than a year, the subscription is separated into terms of up to one year each. Each term has distinct start dates, end dates, and available credit. You can use the available credit at any point during the term, but credit doesn't roll over to any following terms in the subscription. You can get extra flexibility to use credit from terms that haven't yet started by paying up-front for the entire subscription rather than using monthly, quarterly, or another recurring billing cadence. If your usage exceeds your available credit, the extra usage is billed as overage at the non-discounted rate.

For example, say that you buy an {{site.data.keyword.cloud_notm}} platform subscription for $1,000 a month for two years, and the subscription starts 1 July 2019. The subscription is divided into two terms that each contain $12,000 of credit, with one term valid from 1 July 2019 through 30 June 2020, and the next term valid from 1 July 2020 through 30 June 2021. You can use the $12,000 credit of the first term at any time during its one-year period, whether it's $6,500 the first month and $500 a month afterward or $1,000 each month. If you spend $13,000 during that time period and don't have any other active subscriptions, the extra $1,000 is billed as overage.

If you have multiple subscriptions in your account that are valid at the same time, credit is spent from the individual subscription terms according to which one expires the soonest. Adding to the previous example, you might buy a new one-year subscription, `00432100`, for $750 a month that starts 1 September 2019. As users in your account use resources, credit is deducted from the first term of your existing subscription, `01234567`, because it expires first. When all its credit is spent, credit is then deducted from subscription `00432100` while it's valid.

| Subscription | Credit | Valid From | Valid Until |
| ------------ | ---------------- | ---------- | ----------- |
| {{site.data.keyword.Bluemix_notm}} Platform - 01234567, term 1 | $12,000 | 1 July 2019 | 30 June 2020 |
| {{site.data.keyword.Bluemix_notm}} Platform - 00432100 | $9,000 | 1 September 2019 | 31 August 2020 |
| {{site.data.keyword.Bluemix_notm}} Platform - 01234567, term 2 | $12,000 | 1 July 2020 | 30 June 2021 |
{: caption="Table 1. Subscription credit spending order" caption-side="top"}

Support subscriptions that you buy after 24 September 2019 can be spent as described in this section, with credit being available for the entire subscription term. For support subscriptions that were bought before this date, credit is available on a month-to-month basis. When you buy or renew a support subscription, any existing active support subscriptions are converted to the term-based model for the remainder of their term. <br><br>For example, you might have a support subscription for $200 per month with three months remaining. When you buy a new support subscription, the existing subscription is converted to a new one with $600 of credit that can be used any time within those three months.
{: note}

## Viewing subscription usage
{: #subscription-usage}

You can view the subscriptions in your account to track your credit spending. To access this information, you need an access policy with the Administrator role on the Billing account management service. See [IAM access](/docs/iam?topic=iam-userroles) for more information.

### Platform subscriptions
{: #platform-service-subscriptions}

To view your platform and service subscription usage, go to **Manage > Billing and usage**, and select **Subscriptions**.

  * Click the tabs to view spending details and trends about your subscription usage, including any usage overages that your account incurred. For example, the credit burndown view displays how your credit balance has changed over time, and the spending by month view displays your monthly spending from all subscriptions.
  * View all active and inactive subscriptions in your account in the tables. For multi-year subscriptions, each term is displayed separately. Active subscriptions are subscriptions that still have remaining credit to spend and time that's left in the subscription term. Upcoming subscriptions are subscriptions were added to the account but haven't yet reached their term period. A subscription is inactive if its term expires or all of its credit is spent.

You can use the spending and usage information on the Subscriptions page to evaluate whether your subscriptions suit your usage needs. For example, if you consistently have overages, you might increase your monthly spending commitment to save money on that usage. To buy new subscriptions or change future subscription amounts, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg).

### Support subscriptions
{: #view-support-subscriptions}

To view support subscription usage, go to **Manage > Billing and usage**, and select **Support costs**. You can view the remaining credit in your active support subscriptions and any upcoming subscriptions that aren't yet valid. For more information, see [Viewing your support costs](/docs/billing-usage?topic=billing-usage-support).

## Adding subscription credit
{: #subscription-codes}

After you buy a subscription for platform or support credit, you add the credit to your account by applying a subscription code. Applying the code ensures that the credit is added to your account and you don't have unexpected overage charges.

If you set up your first subscription through the Subscriptions page, the credit for this subscription is automatically added to your account - no code required.
{: tip}

After {{site.data.keyword.Bluemix_notm}} Sales places the order, an email with the subscription code for each subscription and support line item is sent to the appropriate contact. If you bought a subscription and didn't receive your subscription code, [contact us ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} or email Sales at CloudDigitalSales@us.ibm.com to request for it to be sent again.

Only the account owner or a user with the Editor or Administrator role on the Billing account management service can apply the subscription code. If you don't have access to apply subscription codes, the account owner or administrator can provide access. See [Assigning access to account management services](/docs/iam?topic=iam-account-services) for more information.

1. From the {{site.data.keyword.Bluemix_notm}} console, go to **Manage > Account**, and select **Account settings**.
1. Click **Apply code**.

  Each code can be redeemed only once, and the codes must be redeemed before their expiration date. Credit that is added to an account cannot be removed.
  {: important}

1. Enter the subscription code, and click **Apply**.

   If you have separate codes for platform and support credit, apply the platform subscription code first, then apply the support subscription code.

If you don't know your seller, the codes are applied in the wrong order, or you experience issues with applying the codes, [contact {{site.data.keyword.Bluemix_notm}} Support](/docs/get-support?topic=get-support-getting-customer-support).
