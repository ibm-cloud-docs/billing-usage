---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-19"

keywords: view usage, view cost, service usage, usage report, usage permissions, usage details

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'} 
{:new_window: target="_blank"}
{:tip: .tip}


# Viewing your usage
{: #viewingusage}

You can view your {{site.data.keyword.cloud}} usage details, including a summary of estimated charges for all services and resources that are used per month in your organizations, from the Usage page in the console.
{:shortdesc}

## Before you begin
{: #view-usage-permissions}

Ensure that you have the access that's required to view usage data for the resources. Access can be assigned at the account level or to individual resource groups and Cloud Foundry orgs.
* To view usage for all resources in the account, you need an access policy with the Administrator role on the Billing account management service. 
* To view usage only for specific {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) resources, you need the Viewer role on the resource group.
*  To view usage for a resource group, you must be the administrator on the account to grant users the viewer role or higher on the Billing account management service. You can set access to view the usage data on one or more resource groups for the billing service.
* To view usage only for specific Cloud Foundry services, the Billing manager role must be applied at the org level. Billing managers can see the details for only the organizations in which they are assigned the Billing manager role.

For more information about access roles, see [IAM access](/docs/iam?topic=iam-userroles) and [Cloud foundry access](/docs/iam?topic=iam-cfaccess).

## Viewing service usage details
{: #services}
{: help} 
{: support}

In the Services section, you can view a list of your services and the estimated costs that are associated with those services. To view a summary of estimated charges for all instances of a specific resource, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, go to **Manage > Billing and usage**, and select **Usage**.
2. Click **View plans** to view all the instances of a specific type of resource.  
3. To see a detailed summary of estimated charges for each instance of a specific resource type, click **View details**. You can also see the detailed monthly usage metrics for the selected instance.

The account is billed for the total usage that is incurred across all groups and organizations at the end of each billing cycle. Each billing cycle lasts one month.

You can filter the usage summary by group and select the time frame for usage. The charges that are shown represent the amount that is billed to the account for that particular month.

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

   You can use the **Tags** column in the instance CSV file to help analyze the resources in your account. For example, you might have multiple projects in an account, each with a Kubernetes cluster and a few Cloud Foundry app deployments. You can organize the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. For more information about tagging, see [Working with tags](/docs/resources?topic=resources-tag).
   {: tip}
