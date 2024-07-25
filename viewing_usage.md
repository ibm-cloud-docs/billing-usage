---

copyright:
  years: 2017, 2024
lastupdated: "2024-07-25"

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

Ensure that you have the required access to view usage data for the resources. Access can be assigned at the account-level or to individual resource groups.
* To view usage for all resources in the account, you need an access policy with the Administrator role on the Billing account management service.
* To view usage only for specific {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) resources, you need the Viewer role on the resource group.

You can limit the access to view the usage for a specific resource group by assigning the viewer role or higher on all Identity and Access enabled services within that resource group.
{: note}

For more information about access roles, see [IAM access](/docs/account?topic=account-userroles).

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


### Viewing usage details from the cost analysis page
{: #cost-analysis-page}

This is a beta feature that is available for evaluation and testing purposes.
{: beta}

From the cost analysis page you can view your accounts usage by comparing costs over several months as well as filtering the usage to view cost by region, service, plan, instance, instance ID, and resource group.

The cost analysis page is only available to standalone accounts and enterprise child accounts. Enterprise root accounts can't view the page.
{: note}

You need an IAM access policy with the Operator role or higher on the Billing account management service. To view the cost analysis page, in the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Cost analysis**.

When using the cost analysis page, you can use the group by filter to dive deeper into your accounts usage. For example, you can select **Service** from the group by dropdown and the chart will display your usage across all of your account's services. You can add **Region** from the group by dropdown, and now the chart will display your services and the regions where there's usage. Hover over one of the month's bars, and you can view the grouping of the service and region involved. Use that information to further filter the chart. If you view the hover text and see `us-south`, for example, and filter just for `us-south` in the Region dropdown and get more insights into the usage for that region.

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

   You can use the tag related columns in the instance CSV file to help analyze the resources in your account. For example, you might have multiple projects in an account, each with a Kubernetes cluster. You can organize the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. For more information about tagging, see [Working with tags](/docs/account?topic=account-tag).
   {: tip}

   Consider creating tags as a `key:value` pair to group related tags. The `key` becomes a column in the CSV file and the `value` is populated in the respective rows of the column. If you don't follow a `key:value` tag style, the tags appear in the **Other Tags** column.
   {: tip}



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
