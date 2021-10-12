---

copyright:
  years: 2017, 2021
lastupdated: "2021-10-11"

keywords: view usage, view cost, service usage, usage report, usage permissions, usage details

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:tip: .tip}
{:note: .note}
{:important:  .important}
{:api: .ph data-hd-interface='api'}
{:cli: .ph data-hd-interface='cli'}
{:ui: .ph data-hd-interface='ui'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}


# Viewing your usage
{: #viewingusage}

You can view your {{site.data.keyword.cloud}} usage details, including a summary of estimated charges for all services and resources that are used per month in your organizations, from the Usage page in the console.
{: shortdesc}

## Before you begin
{: #view-usage-permissions}

Ensure that you have the access that's required to view usage data for the resources. Access can be assigned at the account level or to individual resource groups and Cloud Foundry orgs.
* To view usage for all resources in the account, you need an access policy with the Administrator role on the Billing account management service. 
* To view usage only for specific {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) resources, you need the Viewer role on the resource group.
* To view usage only for specific Cloud Foundry services, the Billing manager role must be applied at the org level. Billing managers can see the details for only the organizations in which they are assigned the Billing manager role.

You can limit the access to view the usage for a specific resource group by assigning the viewer role or higher on all Identity and Access enabled services within that resource group.
{: note} 

For more information about access roles, see [IAM access](/docs/account?topic=account-userroles) and [Cloud foundry access](/docs/account?topic=account-cfaccess).

## Viewing service usage details
{: #services}
{: help} 
{: support}

In the Services section, you can view a list of your services and the estimated costs that are associated with those services. To view a summary of estimated charges for all instances of a specific resource, complete the following steps:

### Viewing service usage details in the console 
{: #usage-ui}
{: ui} 

1. In the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Usage**.
2. Click **View plans** to view all the instances of a specific type of resource.  
3. To view a detailed summary of estimated charges for each instance of a specific resource type, click **View details**. You can also view the detailed monthly usage metrics for the selected instance.

If you have a Pay-As-You-Go account that isn't billed in US dollars or a Subscription account, the usage for all services is finalized by the 20th of the following month. If you have a Pay-As-You-Go account that is billed in US dollars, the usage for all services is finalized by the 3rd of the following month.
{: important}

The account is billed for the total usage that is incurred across all groups and organizations at the end of each billing cycle. Each billing cycle lasts one month.

You can filter the usage summary by group and select the timeframe for usage. The charges that are shown represent the amount that is billed to the account for that particular month.

If you select a specific organization from the **Filter by group** list, you can see the total usage for that organization, including any usage as part of a free tier. The free tier usage is shown as free at the account level, but not at the organizational level. When you view the organizational usage, you see the real usage for that organization, which includes both free and charged usage. All organizational usage is rolled up to the account usage after the free tier is removed.

The account owner of a billable account can set spending notifications against the total cost of the account, for runtime, services, and for individual services, excluding third-party services. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).

## Exporting your usage details to a `.csv` file
{: #export-csv}
{: help} 
{: support}

You can export a summary of your account's usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. Because the report includes usage data for the entire account, you need Administrator access on the Billing service to export usage details.

1. In the console, go to **Manage > Billing and usage**, and select **Usage**.
1. Click **Export CSV** and select one of the options:
   - Click **Summary** for a high-level overview of the usage and associated costs for your account.
   - Click **Instance** for detailed usage information about each service instance.

   You can use the **Tags** column in the instance CSV file to help analyze the resources in your account. For example, you might have multiple projects in an account, each with a Kubernetes cluster and a few Cloud Foundry app deployments. You can organize the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. For more information about tagging, see [Working with tags](/docs/account?topic=account-tag).
   {: tip}

   Consider creating tags as a key:value pair to group related tags. The key becomes a column in the CSV file and the pairs are populated in the respective rows of the column. If you don't follow a key:value tag style, the tags appear in the other tags column.
   {: tip}


### Viewing your usage by using the CLI
{: #usage_command_line}
{: cli}

As an alternative to the console, you can view your usage by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI). Use the following commands to retrieve resource usage and billing information.

1. Log in, and select the account.

   ```
   ibmcloud login
   ```
   {: codeblock}

1. View usage by running the **`ibmcloud billing`** command as shown in the following examples.

   * View usage for the current month.

      ```
      ibmcloud billing account-usage [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly usage for an org (account admin or org billing manager only):

      ```
      ibmcloud billing org-usage ORG_NAME [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly usage for a resource group (account admin or resource group admin only):

      ```
      ibmcloud billing resource-group-usage GROUP_NAME [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

   * View monthly resource instances usage under the current account:

      ```
      ibmcloud billing resource-instances-usage [-o ORG] [-g RESOURCE_GROUP] [-d YYYY-MM] [--output FORMAT] [-q, --quiet]
      ```
      {: codeblock}

### Viewing your usage by using the API
{: #view-usage-api}
{: api}

You can programmatically view your usage by calling the [{{site.data.keyword.cloud_notm}} Usage Reports API](/apidocs/metering-reporting?code=python#get-account-usage)  You can base the query in your API call on an account, org, resource group, or resource instance. 

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

```
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
