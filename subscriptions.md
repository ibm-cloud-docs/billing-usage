---

copyright:
  years: 2019, 2024
lastupdated: "2024-08-28"

keywords: subscription, credit, subscription code, support code, subscription overage, subscription usage, feature code, expiring subscription, expired subscription

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Managing subscriptions
{: #subscriptions}

With an {{site.data.keyword.cloud}} subscription, you get discounted usage for platform services and support by committing to a minimum spending commitment for a certain period of time. You can buy your first subscription, add more subscriptions, and monitor subscription usage on the Subscriptions page in the {{site.data.keyword.cloud_notm}} console.
{: shortdesc}

If you buy a subscription, your account is converted to a Subscription account type. For more details about other benefits of Subscription accounts, see [Account types](/docs/account?topic=account-accounts).
{: tip}

## How subscription credit is spent
{: #subscription-basics}

Subscriptions can provide the following two types of credit, which are divided into separate pools:
* Credit from platform subscriptions that pays for resource usage
* Credit from support subscriptions that pays for support costs

Each platform or support subscription is purchased for a given credit amount and duration. If the subscription duration is more than a year, the subscription is separated into terms of up to one year each. Each term has distinct start dates, end dates, and available credit. You can use the available credit at any point during the term, but credit doesn't roll over to any following terms in the subscription. You can get flexibility to use credit from terms that haven't yet started by paying up-front for the entire subscription rather than using monthly, quarterly, or another recurring billing cadence. If your usage exceeds your available credit, the additional usage is billed as overage at the non-discounted rate.

For example, say that you buy an {{site.data.keyword.cloud_notm}} platform subscription for $1,000 a month for two years, and the subscription starts 1 July 2019. The subscription is divided into two terms that each contain $12,000 of credit, with one term valid from 1 July 2019 through 30 June 2020, and the next term valid from 1 July 2020 through 30 June 2021. You can use the $12,000 credit of the first term at any time during its one-year period, whether it's $6,500 the first month and $500 a month afterward or $1,000 each month. If you spend $13,000 during that time period and don't have any other active subscriptions, the additional $1,000 is billed as overage.

If you have multiple subscriptions in your account that are valid at the same time, credit is spent from the individual subscription terms according to which one expires the soonest. Adding to the previous example, you might buy a new one-year subscription, `00432100`, for $750 a month that starts 1 September 2019. As users in your account use resources, credit is deducted from the first term of your existing subscription, `01234567`, because it expires first. When all its credit is spent, credit is then deducted from subscription `00432100` while it's valid.

| Subscription | Credit | Valid From | Valid Until |
| ------------ | ---------------- | ---------- | ----------- |
| {{site.data.keyword.Bluemix_notm}} Platform - 01234567, term 1 | $12,000 | 1 July 2019 | 30 June 2020 |
| {{site.data.keyword.Bluemix_notm}} Platform - 00432100 | $9,000 | 1 September 2019 | 31 August 2020 |
| {{site.data.keyword.Bluemix_notm}} Platform - 01234567, term 2 | $12,000 | 1 July 2020 | 30 June 2021 |
{: caption="Subscription credit spending order" caption-side="top"}

If you have multiple subscriptions in your account that have terms greater than 12 months and you pay up-front for the entire subscription rather than using monthly, quarterly, or another recurring billing cadence, you won't receive an overage for spending faster than you planned.

For example, say you commit to spending $12,000 per year for 3 years and pay up-front. By month 10, you've consumed the first year's $12,000 credit and spend $2,000 in month 11. Instead of receiving an overage charge, we deduct $2,000 from the third year's credit leaving a balance of $10,000 remaining to spend in year 3. Assuming there are no other charges from the second year's spending, you have $10,000 to spend in year 3 before any overage charges are applied.

Support subscriptions that you buy after 24 September 2019 can be spent as described in this section, with credit being available for the entire subscription term. For support subscriptions that were bought before this date, credit is available on a month-to-month basis. When you buy or renew a support subscription, any existing active support subscriptions are converted to the term-based model for the remainder of their term. \n For example, you might have a support subscription for $200 per month with three months remaining. When you buy a new support subscription, the existing subscription is converted to a new one with $600 of credit that can be used anytime within those three months.
{: note}

## Viewing subscription usage
{: #subscription-usage}
{: help}
{: support}

You can view the subscriptions in your account to track your credit spending. To access this information, you need an access policy with the Viewer role or higher on the Billing account management service. See [IAM access](/docs/account?topic=account-userroles) for more information.

### Platform subscriptions
{: #platform-service-subscriptions}

To view your platform and service subscription usage, in the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Subscriptions**.

* Click the tabs to view spending details and trends about your subscription usage, including any usage overages that your account incurred. For example, the credit burndown view displays how your credit balance changes over time, and the usage by month view displays your monthly usage from all subscriptions.
* View all active and upcoming subscriptions in your account in the tables. For multi-year subscriptions, each term is displayed separately. Active subscriptions are subscriptions that still have remaining credit to spend and time that's remaining in the subscription term. Upcoming subscriptions are subscriptions were added to the account but haven't yet reached their term period.

You can use the spending and usage information on the Subscriptions page to evaluate whether your subscriptions suit your usage needs. For example, if you consistently have overages, you might increase your monthly spending commitment to save money on that usage. To buy new subscriptions or change future subscription amounts, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external}.

### Support subscriptions
{: #view-support-subscriptions}

To view support subscription usage, in the console, go to **Manage > Billing and usage**, and select **Support costs**. You can view the remaining credit in your active support subscriptions and any upcoming subscriptions that aren't yet valid. For more information, see [Viewing your support costs](/docs/billing-usage?topic=billing-usage-support).

## Subscription credit
{: #subscription-codes}

After you buy a subscription for platform or support credit, you add the credit to your account by applying a subscription code. Applying the code ensures that the credit is added to your account and you don't have unexpected overage charges.

For more information, see [Applying subscription codes](/docs/billing-usage?topic=billing-usage-subscription_code).

## Expiring subscriptions
{: #expiring-subscription-date}
{: help}
{: support}

You are notified by email and on the [Subscriptions](/billing/subscriptions) page 60, 30, 14, and 1 day before the expiration date of the last subscription on the account. A subscription is inactive if its term expires or all of its credit is spent. After the subscription expires, your account is converted to a Pay-As-You Go account, which means you pay only for billable services that you use with no contracts or commitments. The discounts that are associated with the subscription account don't apply to the Pay-As-You-Go account. To avoid getting charged at the Pay-As-You-Go, rate, set up a new subscription with Sales before the expiration date of the last subscription on the account.

To learn more, see [Pay-As-You-Go accounts](/docs/account?topic=account-accounts#paygo).
