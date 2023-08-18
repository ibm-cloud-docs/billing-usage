---

copyright:
  years: 2017, 2023
lastupdated: "2023-08-18"

keywords: view usage, view cost, service usage, usage report, usage permissions, usage details

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}


# Viewing your usage
{: #viewingusage}

You can view your {{site.data.keyword.cloud}} usage details from the billing and usage dashboard or from the Usage page in the console. Your usage details include a summary of estimated charges for all services and resources that are used per month in your organizations.
{: shortdesc}

## Before you begin
{: #view-usage-permissions}

Ensure that you have the required access to view usage data for the resources. Access can be assigned at the account-level or to individual resource groups and Cloud Foundry orgs.
* To view usage for all resources in the account, you need an access policy with the Administrator role on the Billing account management service.
* To view usage only for specific {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) resources, you need the Viewer role on the resource group.
* To view usage only for specific Cloud Foundry services, the Billing manager role must be applied at the org level. Billing managers can see the details for only the organizations in which they are assigned the Billing manager role.

You can limit the access to view the usage for a specific resource group by assigning the viewer role or higher on all Identity and Access enabled services within that resource group.
{: note}

For more information about access roles, see [IAM access](/docs/account?topic=account-userroles) and [Cloud foundry access](/docs/account?topic=account-cfaccess).

## Viewing service usage details in the console
{: #services}
{: help}
{: support}
{: ui}

The usage summary widget provides a view of your month-to date-spending, last month spending, average monthly spending, and next month's predicted usage at a glance. For a more granular view of your usage and specific costs that are associated with services, view your usage from the usage page.

### Viewing usage details from the usage summary widget
{: #usage-summary}

In the usage summary widget on the billing and usage dashboard, you get view of your actual and predicted spending trends.

The predicted usage for the next month is calculated by finding the trend from the usage of the last three months, including the current month. For example, if it's August, predicted usage is calculated based on usage trends in June, July, and August to find the predicted usage for September.

Let's say the usage is $950.00 USD for June, $1000.00 USD for July, and $1012.50 USD for August. The difference is calculated between the current month and the last month, and last month and the month before that. Then, the two calculations are averaged to find the trend. That trend amount of $1043.75 USD is the predicted next month's usage, with the following calculations:

* Change between August and July = $1012.50 - $1000.00 = $12.50 USD
* Change between July and June = $1000.00 - $950.00 = $50.00 USD
* Average change (trend) = ($12.50 + $50.00) / 2 = $31.25 USD

August usage ($1012.50) + Average change ($31.25) = The predicted usage for next month September ($1043.75 USD)

### Viewing usage details from the usage page
{: #usage-details-page}

In the Services section, you can view a list of your services and the estimated costs that are associated with those services. To view a summary of estimated charges for all instances of a specific resource, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Usage**.
2. Click **View plans** to view all the instances of a specific type of resource.
3. To view a detailed summary of estimated charges for each instance of a specific resource type, click **View details**. You can also view the detailed monthly usage metrics for the selected instance.

If you have a Pay-As-You-Go account that isn't billed in US dollars or a Subscription account, the usage for all services is finalized by the 20th of the following month. If you have a Pay-As-You-Go account that is billed in US dollars, the usage for all services is finalized by the 3rd of the following month.
{: important}

The account is billed for the total usage that is incurred across all groups and organizations at the end of each billing cycle. Each billing cycle lasts one month.

You can filter the usage summary by group and select the time frame for usage. The charges that are shown represent the amount that is billed to the account for that particular month.

If you select a specific organization from the **Filter by group** list, you can see the total usage for that organization, including any usage as part of a free tier. The free tier usage is shown as free at the account level, but not at the organizational level. When you view the organizational usage, you see the real usage for that organization, which includes both free and charged usage. All organizational usage is rolled up to the account usage after the free tier is removed.

The account owner of a billable account can set spending notifications against the total cost of the account, for runtime, services, and for individual services, excluding third-party services. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).

## Viewing your usage by using the API
{: #view-usage-api}
{: api}

You can programmatically view your usage by calling the [{{site.data.keyword.cloud_notm}} Usage Reports API](/apidocs/metering-reporting#get-account-usage). You can base the query in your API call on an account, org, resource group, or resource instance.

The following examples show queries that you can use to view account level usage:

```bash
curl -X GET -H "Authorization: {iam_token}" -H "Accept: application/json" "{base_url}/v4/accounts/{account_id}/usage/{billingmonth}"
```
{: pre}
{: curl}

```java
ServiceCall<AccountUsage> getAccountUsage(GetAccountUsageOptions getAccountUsageOptions)
```
{: codeblock}
{: java}

```javascript
getAccountUsage(params)
```
{: codeblock}
{: javascript}

```python
get_account_usage(self,
        account_id: str,
        billingmonth: str,
        *,
        names: bool = None,
        accept_language: str = None,
        **kwargs
    ) -> DetailedResponse
```
{: codeblock}
{: python}

```go
(usageReports *UsageReportsV4) GetAccountUsage(getAccountUsageOptions *GetAccountUsageOptions) (result *AccountUsage, response *core.DetailedResponse, err error)
```
{: codeblock}
{: go}

## Exporting your usage details to a CSV file
{: #export-csv}
{: help}
{: support}
{: ui}

You can export a summary of your account's usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. Because the report includes usage data for the entire account, you need Administrator access on the Billing service to export usage details.

This is not an estimate of your final bill. Instance costs don’t reflect your final bill because other charges or discounts might be applied to your account.
{: note}

1. In the console, go to **Manage > Billing and usage**, and select **Usage**.
1. Click **Export CSV** and select one of the options:
   - Click **Summary** for a high-level overview of the usage and associated costs for your account.
   - Click **Instance** for detailed usage information about each service instance.

   You can use the tag related columns in the instance CSV file to help analyze the resources in your account. For example, you might have multiple projects in an account, each with a Kubernetes cluster and a few Cloud Foundry app deployments. You can organize the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. For more information about tagging, see [Working with tags](/docs/account?topic=account-tag).
   {: tip}

   Consider creating tags as a `key:value` pair to group related tags. The `key` becomes a column in the CSV file and the `value` is populated in the respective rows of the column. If you don't follow a `key:value` tag style, the tags appear in the **Other Tags** column.
   {: tip}

## Exporting your usage details to a CSV file by using the API
{: #export-csv-api}
{: api}

You can export a summary of your account's usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. Because the report includes usage data for the entire account, you need Administrator access on the Billing service to export usage details.

This is not an estimate of your final bill. Instance costs don’t reflect your final bill because other charges or discounts might be applied to your account.
{: note}


### Exporting your account summary CSV report by using the API
{: #export-csv-api-acc-summary}
{: api}

The following examples show queries that you can use to download your account summary CSV report:

```bash
curl -X GET -H "Authorization: {iam_token}" "{base_url}/v4/accounts/{account_id}/summary/{month}?format=csv"
```
{: pre}
{: curl}

This API returns the summary of the account for a given month in a CSV file, and the aggregated usage of each resource plan metric.

#### Understanding CSV table headings and JSON report fields for account summary
{: #export-csv-api-table-account-summary-csv}
{: api}

The following table shows the correlation between the heading titles in your CSV report and JSON report fields. For more information about JSON report fields, see [Usage Reports: Get account summary](/apidocs/metering-reporting#get-account-summary){: external}. Each row of the **Account Resource Usage** section represents the aggregated usage of a service plan metric for all the resource instances in the account.

| CSV Header       | Description                                      |
|---------------------|--------------------------------------------------|
| Account Owner ID    | ID of the account                    |
| Account Name        | Name of the account                  |
| Billing Month       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate       | Currency Exchange Rate with USD as the base     |
| Created Time        | Timestamp at which the CSV report was generated|
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-summary"}
{: #account-owner-id}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|-------------------------------|-------------|
| Account ID          | `account_id`                  | ID of the account |
| Month               | `month`                       | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Country Code        | `billing_country_code`        | Country the requested account is mapped to |
| Currency Code       | `billing_currency_code`       | The currency in which the account is billed |
| Billable Cost       | `resources.billable_cost`     | The billable charges for all cloud resources used in the account |
| Non Billable Cost  | `resources.non_billable_cost` | Non-billable charges for all cloud resources used in the account |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account usage summary" caption-side="bottom"}
{: tab-group="account-summary"}
{: #account-id}
{: tab-title="Account Usage Summary"}

| CSV Header       | JSON Report Fields                                          | Description |
|---------------------|-------------------------------------------------------------|-------------|
| Subscription ID | `subscription.subscriptions.subscription_id`                | The ID of the subscription |
| CA                  | `subscription.subscriptions.charge_agreement_number`        | The charge agreement number of the subscription |
| Type                | `subscription.subscriptions.type`                           | Type of subscription |
| Subscription Amount | `subscription.subscriptions.subscription_amount`            | The credits available in the subscription for the month |
| Start               | `row.subscription.subscriptions.start` or \n `subscription.subscriptions.terms.start`| Pay-As-You-Go accounts: the date from which the subscription was active \n Subscription accounts: The start date of the term |
| End                 | `row.subscription.subscriptions.end` or \n `subscription.subscriptions.terms.end`           | Pay-As-You-Go accounts: unavailable \n Subscription accounts: The end date of the term |
| Credits Total       | `row.subscription.subscriptions.credits_total` or \n `subscription.subscriptions.terms.credits.total`             | Pay-As-You-Go accounts: The total credits available in the  subscription \n Subscription accounts: The total credits available for the term  |
| Credits Starting    | `subscription.subscriptions.terms.credits.starting_balance` | The unused credits in the term at the beginning of the month |
| Credits Used        | `subscription.subscriptions.terms.credits.used`             | The credits used in this month |
| Credits Balance     | `subscription.subscriptions.terms.credits.balance`          | The remaining credits in this term |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for subscriptions" caption-side="bottom"}
{: tab-group="account-summary"}
{: #subscription-id}
{: tab-title="Subscriptions"}

| CSV Header       | JSON Report Fields                     | Description |
|---------------------|-----------------------------------|-------------|
| Offer ID            | `offers.offer_id`                 | The ID of the offer |
| Credits Total       | `offers.credits_total`            | The total credits before applying the offer |
| Offer Template      | `offers.offer_template`           | The template with which the offer was generated |
| Valid From          | `offers.valid_from`               | The date from which the offer is valid |
| Expire Date         | `offers.expires_on`               | The date until the offer is valid |
| Recurring           | `offers.is_recurring`             | Indicates if a cost is recurring |
| Starting Balance    | `offers.credits.starting_balance` | The available credits in the offer at the beginning of the month |
| Used                | `offers.credits.used`             | The credits used in this month |
| Balance             | `offers.credits.balance`          | The remaining credits in the offer |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for offers" caption-side="bottom"}
{: tab-group="account-summary"}
{: #offer-id}
{: tab-title="Offers"}

| CSV Header       | JSON Report Fields | Description |
|---------------------|--------------------|-------------|
| Support Cost        | `support.cost`     | The monthly support cost |
| Support Type        | `row.support.type` \n (`STANDARD` > `Advanced` and \n `PREMIUM` > `Premium`) | The type of support  |
| Support Overage     | `support.overage`  | Additional support cost for the month |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for support summary" caption-side="bottom"}
{: tab-group="account-summary"}
{: #support-cost}
{: tab-title="Support Summary"}

| CSV Header  | JSON Report Fields                 | Description |
|----------------|------------------------------------|-------------|
| Service Name   | `resources.resource_name`          | The name of the resource |
| Service ID     | `resources.resource_id`            | The ID of the resource |
| Currency       | `currency_code`                    | The currency for the cost fields in the resources, plans, and metrics |
| Billable       | `resources.billable`               | Indicates if the plan charges are billed to the customer |
| Plan Name      | `resources.plan_name`              | Name of the service plan |
| Plan ID        | `resources.plan_id`                | ID of the service plan |
| Pricing Region | `reports.resources.plans.pricing_region` | Pricing region for the plan |
| Metric         | `resources.usage.metric`           | The ID of the metric |
| Unit           | `resources.usage.unit`             | The unit that qualifies the quantity |
| Quantity       | `resources.usage.quantity`         | The aggregated value for the metric |
| Cost           | `resources.usage.cost`             | The cost incurred by the metric |
| Original Cost  | `resources.usage.rated_cost`       | Pre-discounted cost incurred by the metric |
| Pending        | `row.resources.pending`            | Pending charge from classic infrastructure |
| Discount (%)   | `row.resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID    | `row.resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
{: class="simple-tab-table"}
{: caption="Table 1. Account summary CSV header titles and JSON report fields for account resource usage" caption-side="bottom"}
{: tab-group="account-summary"}
{: #service-name}
{: tab-title="Account Resource Usage"}


### Exporting your instance CSV report by using the API
{: #export-csv-api-instance}
{: api}

The following examples show queries that you can use to download your instance CSV report:

```bash
curl -X GET -H "Authorization: {iam_token}" "{base_url}/v4/accounts/{account_id}/resource_instances/usage/{month}?format=csv"
```
{: pre}
{: curl}


#### Understanding CSV table headings and API parameters for instances
{: #table-account-summary-csv}
{: api}

The following table shows the correlation between the heading titles in your CSV report and API parameters. For more information about JSON report fields, see [Usage Reports: Get resource instance usage in an account](/apidocs/metering-reporting#get-resource-usage-account). Each row of the **Account Instance Usage** section represents an instance usage of a specific metric in a service plan.

Regular account CSV reports are not real time and can be incomplete. Complete CSV reports are generated for previous months that have already been invoiced. In case of potentially inconsistent data in the CSV reports, it's advised to regenerate the CSV after couple of hours. For more accurate and real time usages, it's always recommended to use the JSON APIs.
{: note}

| CSV Header    | Description                                     |
|------------------|-------------------------------------------------|
| Account Owner ID | ID of the account                    |
| Account Name     | Name of the account                  |
| Billing Month    | The month in which usages were incurred. Represented in `yyyy-mm` format     |
| Currency Rate    | Currency Exchange Rate with USD as the base     |
| Created Time     | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 2. Account instance CSV header titles and descriptions for account metadata" caption-side="bottom"}
{: tab-group="account-instance"}
{: #account-owner-id-instance}
{: tab-title="Account Metadata"}

| CSV Header       | JSON Report Fields                 | Description |
|---------------------|------------------------------------|-------------|
| Service Name        | `resources.resource_name`          | The name of the resource |
| Service ID          | `resources.resource_id`            | The ID of the resource |
| Instance Name       | `resources.resource_instance_name` | The name of the resource instance |
| Instance ID         | `resources.resource_instance_id`   | The ID of the resource instance |
| Plan Name           | `resources.plan_name`              | The name of the plan where the instance was provisioned and rated |
| Plan ID             | `resources.plan_id`                | The ID of the plan where the instance was provisioned and rated |
| Region              | `resources.region`                 | The region where instance was provisioned |
| Consumer ID         | `resources.consumer_id`            | The ID of the consumer |
| Resource Group Name | `resources.resource_group_name`    | The name of the resource group |
| Resource Group ID   | `resources.resource_group_id`      | The ID of the resource group |
| CF Org              | `resources.organization_name`      | The name of the CF organization |
| Org ID              | `resources.organization_id`        | The ID of the CF organization |
| CF Space            | `resources.space_name`             | The name of the CF space |
| Space ID            | `resources.space_id`               | The ID of the CF space|
| Currency            | `resources.currency_code`          | The currency for the cost fields in the resources, plans, and metrics |
| Billable            | `resources.billable`               | Validates if a cost is charged to the account |
| Usage Metric        | `resources.usage.metric`           | ID of the metric |
| Usage Unit          | `resources.usage.unit`             | Unit that qualifies the quantity |
| Usage Quantity      | `resources.usage.quantity`         | Aggregated value for the metric |
| Usage Cost          | `resources.usage.cost`             | Cost incurred by the metric |
| Original Cost       | `resources.usage.rated_cost`       | The starting cost of a resource within your account |
| Pending             | `row.resources.pending`            | 	Pending charge from classic infrastructure |
| Discount (%)        | `row.resources.plans.usage.discounts.discount`, semicolon(;) delimited | Discount percentage that is applied to the account |
| Discount ID         | `row.resources.plans.usage.discounts.ref`, semicolon(;) delimited | Reference ID of the discount |
| Other Tags          | `resources.tags`                   | Tags that are not of `key:value` format |
{: class="simple-tab-table"}
{: caption="Table 2. Account instance CSV header titles and JSON report fields for account instance usage" caption-side="bottom"}
{: tab-group="account-instance"}
{: #service-name-instance}
{: tab-title="Account Instance Usage"}

For tags that are of `key:value` format, a new column is added for each and every unique `key`, with the `key` as the column name and the `value` as the column value for the corresponding instance usage row. For example, if there are two instances, `i1` and `i2`, with tag `env:prod` on `i1` and tags `env:test` and `team:backend` on `i2`, there would be two additional columns named `env` and `team`. And only the `i1` row will have value `prod` under the `env` column. The `i2` row will have values `test` and `backend` under the `env` and `team` columns. The following table shows the example layout.

| Instance ID | Other tags | `env`  | `team`    |
|-------------|------------|--------|-----------|
| `i1`        |            | `prod` |           |
| `i2`        |            | `test` | `backend` |
{: caption="Table 3. Example of tag layout in the CSV report" caption-side="bottom"}


## Viewing your usage by using the CLI
{: #usage_command_line}
{: cli}

As an alternative to the console, you can view your usage by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI). Use the following commands to retrieve resource usage and billing information.

1. Log in, and select the account.

   ```sh
   ibmcloud login
   ```
   {: codeblock}

1. View usage by running the **`ibmcloud billing`** command as shown in the following examples.

   * View usage for the current month.

      ```sh
      ibmcloud billing account-usage [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly usage for an org (account admin or org billing manager only):

      ```sh
      ibmcloud billing org-usage ORG_NAME [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly usage for a resource group (account admin or resource group admin only):

      ```sh
      ibmcloud billing resource-group-usage GROUP_NAME [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly resource instances usage under the current account:

      ```sh
      ibmcloud billing resource-instances-usage [-o ORG] [-g RESOURCE_GROUP] [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}
