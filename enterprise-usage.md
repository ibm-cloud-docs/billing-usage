---

copyright:
  years: 2019, 2024
lastupdated: "2024-01-12"

keywords: enterprise usage, view enterprise costs, account group usage, account usage, cost recovery, chargeback, support cost

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}

# Viewing usage in an enterprise
{: #enterprise-usage}

You can track resource and support costs from accounts in your {{site.data.keyword.Bluemix}} enterprise by viewing their usage. The accounts and account groups that you can view usage for depend on your assigned access.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} enterprises enable you to centrally manage multiple {{site.data.keyword.Bluemix_notm}} accounts. As an enterprise user, you can keep an eye on resource usage and the associated costs for any account in the enterprise. See [What is an enterprise?](/docs/secure-enterprise?topic=secure-enterprise-what-is-enterprise) for more information.

## Required access for viewing enterprise usage
{: #enterprise-usage-access}

In an enterprise, access to usage information is controlled by the Enterprise service. To view usage information, users must be invited to the enterprise account and have the Usage Reports Viewer, Editor, or Administrator role on the Enterprise service. The Usage Reports Viewer role provides access only to viewing usage reports, while the Editor and Administrator roles enable additional enterprise management actions. In keeping with security best practices, assign the least amount of access that is needed for the user to complete their task. For more information, see [Enterprise actions and roles](/docs/account?topic=account-account-services#enterprise-account-management).

You can give users granular access so that they can view usage for a certain account or account group. For example, say that your enterprise has account groups for each department, and each department has account groups for each team. You can scope the access so that each enterprise user can see only the information that is needed to fulfill their job role.
* Your financial officer needs to view usage for the entire enterprise so that they can track and recover costs for each department, but they don't need to create accounts or account groups. Assign them the Usage Reports Viewer role for the enterprise.
* Each department lead needs to view usage for their department, and they also need to create and manage accounts and account groups for their teams. Assign each department lead the Editor role for their department's account group.
* Each team lead needs to view their team's usage, but you want them to get department approval to add new accounts to their team. Assign each team lead the Usage Reports Viewer role for their team's account group. They can view usage from all accounts within the account group, but not the usage from the account groups of other teams in the department.

For detailed steps about assigning enterprise access, see [Assigning access for enterprise management](/docs/secure-enterprise?topic=secure-enterprise-assign-access-enterprise).

## Viewing enterprise usage in the console
{: #enterprise-usage-console}
{: ui}

1. Log in to the enterprise account.
1. In the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Usage**.

   The Usage page displays the costs for all resource usage in the entire enterprise during the current month. Usage is organized according to your enterprise hierarchy, so costs are broken down by the accounts and account groups that are directly under the enterprise.

   In the Support section, you can view the total support costs for all accounts within your enterprise. The starting credit reflects the monthly amount in your support subscription. If the support usage for the month was more than this amount, it's displayed as overage.

   Usage information for classic infrastructure services is not included for the current billing period. However, it is included for previous billing periods, which you can view by selecting an earlier month from the **Time frame** menu. For more information, see [Viewing usage for your classic infrastructure resources](/docs/billing-usage?topic=billing-usage-infra-usage).

1. To view usage within an account group, click the account group name in the table or in the **Enterprise level** menu. Similar to the enterprise level, usage is broken down by the account and account group.

   If an account group doesn't contain any accounts, it isn't displayed on the Usage page.

1. To view usage by resource, go to the account level by clicking through account groups in the table or selecting the account from the **Enterprise level** menu. Costs for each type of resource that was used during the time frame are displayed.

   From the enterprise account, you can't view usage data for the resource plan or instance because it requires access within the account. If you're a user in the account, switch to the account to view this data. You need billing access to the resources and services in the account as described in [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

Only data for usage that is incurred by accounts in the enterprise is displayed in the enterprise account. To view usage from before an account was added to the enterprise, log in to that account and select the relevant time frame.
{: note}


## Viewing enterprise usage by using the CLI
{: #enterprise-usage-cli}
{: cli}

You can get a report of usage for the enterprise, an account group, or a specific account.

1. Log in, and select the enterprise account.

   ```
   ibmcloud login
   ```
   {: codeblock}

1. If you want to view usage for a specific account group or account, find the name or ID by running the **`ibmcloud enterprise`** command.

   For example, the following command displays all account groups in an enterprise.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}

1. View usage by running the **`ibmcloud billing`** command as shown in the following examples.

   * View usage for the entire enterprise for the current month.

      ```
      ibmcloud billing enterprise-usage
      ```
      {: codeblock}

   * View usage for the `Development` account group for July 2019.

      ```
      ibmcloud billing enterprise-usage --account-group Development --month 2019-07
      ```
      {: codeblock}

   * View the usage for the account groups and accounts that are directly under the enterprise.

      ```
      ibmcloud billing enterprise-usage --children
      ```
      {:  codeblock}

By default, the commands output the usage report for the current month in the following format. Most costs are listed as billable costs. Non-billable costs are listed only in rare cases, such as for the month when you add a trial account to the enterprise.

   ```
   Name             Type            Billable Cost   Non-billable Cost   Currency   Month
Example Corp     account         123.45          0                   USD        2019-07
Development      account_group   234.56          0                   USD        2019-07
Marketing        account_group   345.67          0                   USD        2019-07
Sales            account_group   456.78          0                   USD        2019-07
   ```
   {: codeblock}

   You can output the report in JSON format by specifying the `--output JSON` option.
   {: tip}

## Viewing enterprise usage by using the API
{: #enterprise-usage-api}
{: api}

You can get usage reports from an enterprise and its accounts by calling the [Enterprise Usage Reports API](/apidocs/enterprise-apis/resource-usage-reports). You can base the query in your API call on an enterprise, an account group, or an account and specify whether to view the entity or its children.

The following examples show queries that you can use to get different usage reports. When you call the API, replace the ID variables and IAM token with the values from your enterprise.

```curl
curl -X GET 'https://enterprise.cloud.ibm.com/v1/resource-usage-reports?enterprise_id=abc12340d4bf4e36b0423d209b286f24&month=2019-07' -H 'Authorization: Bearer <IAM Token>'
```
{: codeblock}
{: curl}

```java
ServiceCall<Reports> getResourceUsageReport(GetResourceUsageReportOptions getResourceUsageReportOptions)
```
{: codeblock}
{: java}

```
getResourceUsageReport(params)
```
{: codeblock}
{: javascript}

```python
get_resource_usage_report(self,
        *,
        enterprise_id: str = None,
        account_group_id: str = None,
        account_id: str = None,
        children: bool = None,
        month: str = None,
        billing_unit_id: str = None,
        limit: int = None,
        offset: str = None,
        **kwargs
    ) -> DetailedResponse
```
{: codeblock}
{: python}

```go
(enterpriseUsageReports *EnterpriseUsageReportsV1) GetResourceUsageReport(getResourceUsageReportOptions *GetResourceUsageReportOptions) (result *Reports, response *core.DetailedResponse, err error)
```
{: codeblock}
{: go}

## Exporting your enterprise usage details to a `.csv` file
{: #export-enterprise-csv}
{: ui}

You can export a summary of your account's usage, child account usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. Because the report includes usage data for the entire account, you need Administrator access on the Billing service to export usage details.

1. In the console, go to **Manage > Billing and usage**, and select **Usage**.
1. Click **Export CSV**.


## Exporting your enterprise usage details to a `.csv` file by using the API
{: #enterprise-usage-csv-api}
{: api}

You can export a summary of your account's usage, child account usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. Because the report includes usage data for the entire account, you need Administrator access on the Billing service to export usage details. To get usage reports from an enterprise and get more information about acceptable parameters, see [Enterprise Usage Reports API (Beta)](/apidocs/enterprise-apis/resource-usage-reports).

The following examples show queries that you can use to download your enterprise account `.csv` report. When you call the API, replace the ID variables and IAM token with the values from your enterprise.

```bash
curl -X GET -H 'Authorization: Bearer <IAM Token>' '{base_url}/v1/resource-usage-reports?month=2023-03&format=csv&recurse=true&enterprise_id={enterprise_id}'
```
{: codeblock}
{: curl}


#### Understanding `.csv` table headings and JSON report fields for enterprise account summary
{: #enterprise-usage-table-account-summary-csv}
{: api}

The following table shows the correlation between the heading titles in your `.csv` report and JSON report fields.

| `.csv` Header      | Description        |
|--------------------|--------------------|
| Entity ID          | ID of the requested entity (`enterprise_id`/`account_group_id`/`account_id`) |
| Entity Type        | Type of the requested entity (enterprise/account_group/account) |
| Billing Month      | The month in which usages were incurred. Represented in `yyyy-mm` format |
| Currency Rate      | Currency Exchange Rate with USD as the base |
| Created Time       | Timestamp at which the CSV report was generated |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for entity metadata" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-metadata}
{: tab-title="Entity Metadata"}

| `.csv` Header      | Description |
|--------------------|-------------|
| Entity ID          | ID of the hierarchy entity |
| Entity Type        | Type of the hierarchy entity |
| Entity Name        | Name of the hierarchy entity |
| Parent Entity ID   | ID of the parent of this hierarchy entity |
| Parent Entity Name | Name of the parent of the current hierarchy entity |
| Parent Entity Type | Type of the parent of the current hierarchy entity |
| Entity CreatedOn   | Timestamp at which the hierarchy entity was created |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for entity hierarchy" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-hierarchy}
{: tab-title="Entity Hierarchy"}

| JSON report section API | `.csv` Header          | JSON Report Fields        | Description        |
|-------------------------|------------------------|---------------------------|--------------------|
| [Enterprise Billing Units: List billing units](/apidocs/enterprise-apis/billing-unit#list-billing-units){: external} | | | |
|                         | Billing Unit ID        | `resources.id`         | The ID of the DEFAULT billing unit of the requested entity, which is a globally unique identifier (GUID) |
|                         | Billing Unit Name      | `resources.name`       | The name of the billing unit |
|                         | Billing Unit CreatedOn | `resources.created_at` | The creation date of the billing unit |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for billing units" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #billing-unit-id-enterprise}
{: tab-title="Billing Units"}

| JSON report section API | `.csv` Header     | JSON Report Fields                        | Description        |
|-------------------------|-------------------|-------------------------------------------|--------------------|
| [Enterprise Billing Units: Get credit pools](/apidocs/enterprise-apis/billing-unit#get-credit-pools){: external} | | | |
|                         | Credit Pool Type  | `resources.type`                          | The type of credit, either `PLATFORM` or `SUPPORT` |
|                         | Currency Code     | `resources.currency_code`                 | The currency code of the associated billing unit |
|                         | Billing Option ID | `resources.term_credits.billing_option_id`| The ID of the billing option from which the subscription term is derived |
|                         | Category          | `resources.term_credits.category`         | The category of the credit pool. \n For platform credit the valid values are `PLATFORM`, `OFFER`, or `SERVICE` \n For support credit the valid value is `SUPPORT` |
|                         | Start Date        | `resources.term_credits.start_date`       | The start date of the term in ISO format |
|                         | End Date          | `resources.term_credits.end_date`         | The end date of the term in ISO format  |
|                         | Total Credits     | `resources.term_credits.total_credits`    | The total credit available in this term |
|                         | Starting Balance  | `resources.term_credits.starting_balance` | The balance of available credit at the start of the current month |
|                         | Used Credits      | `resources.term_credits.used_credits`     | The amount of credit used during the current month |
|                         | Current Balance   | `resources.term_credits.current_balance`  | The balance of remaining credit in the subscription term |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for credit pools" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #credit-pool-type-enterprise}
{: tab-title="Credit Pools"}

| JSON report section API | `.csv` Header     | JSON Report Fields       | Description        |
|-------------------------|-------------------|--------------------------|--------------------|
| [Enterprise Billing Units: Get credit pools](/apidocs/enterprise-apis/billing-unit#get-credit-pools){: external} | | | |
|                         | Credit Pool Type  | `resources.type`         | The type of credit, either `PLATFORM` or `SUPPORT` |
|                         | Currency Code     | `resources.currency_code`| The currency code of the associated billing unit |
|                         | Overage           | `resources.overage.cost` | The number of credits that are used as overage |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for overages" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #overages-enterprise}
{: tab-title="Overages"}

| JSON report section API | `.csv` Header      | JSON Report Fields  | Description        |
|-------------------------|--------------------|---------------------|--------------------|
| [Enterprise Usage Reports API: Get usage reports for enterprise entities](/apidocs/enterprise-apis/resource-usage-reports#get-resource-usage-report){: external} | | | |
|                         | Entity ID          | `entity_id`         | The ID of the entity |
|                         | Entity Type        | `entity_type`       | The type of the entity  \n Possible values: `enterprise` , `account-group`, or `account` |
|                         | Entity Name        | `entity_name`       | A user-defined name for the entity, such as the enterprise name or account group name |
|                         | Billing Unit ID    | `billing_unit_id`   | The ID of the billing unit  |
|                         | Billing Unit Name  | `billing_unit_name` | The name of the billing unit |
|                         | Country Code       | `country_code`      | The country code of the billing unit |
|                         | Currency Code      | `currency_code`     | The currency code of the billing unit |
|                         | Billable Cost      | `billable_cost`     | Billable charges that are aggregated from all entities in the report |
|                         | Non Billable Cost  | `non_billable_cost` | Non-billable charges that are aggregated from all entities in the report |
{: class="simple-tab-table"}
{: caption="Table 1.  Enterprise usage report CSV contents for enterprise usage summary" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-resource-usage1}
{: tab-title="Enterprise Usage Summary"}

| JSON report section API | `.csv` Header    | JSON Report Fields                       | Description        |
|-------------------------|------------------|------------------------------------------|--------------------|
| [Enterprise Usage Reports API: Get usage reports for enterprise entities](/apidocs/enterprise-apis/resource-usage-reports#get-resource-usage-report){: external} | | | |
|                         | Entity ID        | `reports.entity_id`                      | The ID of the entity |
|                         | Entity Type      | `reports.entity_type`                    | The type of the entity. \n Possible values: `enterprise`, `account-group`, or `account` |
|                         | Parent Entity ID | `reports.parent_entity_id`               | The ID of the parent of the requested entity |
|                         | Billing Unit ID  | `reports.billing_unit_id`                | The ID of the billing unit  |
|                         | Currency Code    | `reports.currency_code`                  | The currency code of the billing unit |
|                         | Service Name     | `reports.resources.resource_name`        | The name of the resource |
|                         | Service ID       | `reports.resources.resource_id`          | The ID of the resource |
|                         | Billable         | `reports.resources.plans.billable`       | Whether the plan charges are billed to the customer |
|                         | Plan Name        | `reports.resources.plan_name`            | The name of the plan |
|                         | Plan ID          | `reports.resources.plan_id`              | The ID of the plan |
|                         | Pricing Region   | `reports.resources.plans.pricing_region` | The pricing region for the plan |
|                         | Metric           | `reports.resources.plans.usage.metric`   | The name of the metric |
|                         | Unit             | `reports.resources.plans.usage.unit`     | A unit to qualify the quantity |
|                         | Quantity         | `reports.resources.plans.usage.quantity` | The aggregated value for the metric |
|                         | Cost             | `reports.resources.plans.usage.cost`     | The cost that was incurred by the metric |
|                         | Pending          | `reports.resources.plans.pending`        | Pending charge from classic infrastructure |
{: class="simple-tab-table"}
{: caption="Table 1. Enterprise usage report CSV contents for enterprise resource usage" caption-side="bottom"}
{: tab-group="enterprise-account-summary"}
{: #entity-resource-usage2}
{: tab-title="Enterprise Resource Usage"}


When `recurse=true`, the usage in the **Enterprise Resource Usage** section is aggregated by each metric of a service plan and it's broken down by child accounts. Each row represents the total usage of a service plan metric in some child account. When `recurse=false`, the usage is aggregated by each metric of a service plan and each row represents the total usage of a service plan metric of all the sub-accounts or child-accounts in the requested entity hierarchy. In the Hierarchy section, `recurse=true` shows all the child entities of the requested entity, and for `recurse=false`, it shows only the direct children of the requested entity.
{: note}


## Recovering costs for enterprise usage
{: #enterprise-cost-recovery}
{: ui}

An enterprise consolidates billing from all of its accounts and account groups to a single invoice, which simplifies billing management. You can recover the costs from resource usage in the enterprise by charging the usage costs for each account group or account to the associated department or team.

To view your enterprise hierarchy and any usage, you need an access policy with the Editor or Administrator role on the Enterprise service for the entire enterprise. The following steps use the {{site.data.keyword.Bluemix_notm}} console as an example, but you can also perform these steps by using the CLI or API.

1. Find the usage costs for each department by going to **Manage > Usage** in the enterprise account. From the **Time frame** menu, select the previous month to view the usage that is included in the latest invoice.

   The costs for your account groups are listed in the table. These costs include all charges except any tax that's charged in your billing region. If you want a further breakdown of usage costs, click the account group name to view the accounts and account groups that it contains.

1. Identify the departments within your company that correspond with the account groups.

   If the contacts that are assigned to your account groups are associated with the department that you want to recover costs from, finding the contact is one way to find this information. Go to **Manage > Enterprise** and select **Accounts**. The contact for each account group is listed in the table.

   However, billing practices vary by company. For example, the account group contact might be a technical focal that's not associated with the department that you want to charge. Always verify the correct department according to your company's accounting processes.

   If your company uses billing codes to charge back costs to departments, add the billing code to the account group name to easily identify the code. For example,`Sales - A2B3`.
   {: tip}

1. Pair the usage costs for each account group with the identified department, and follow your company's processes to submit the charges.
