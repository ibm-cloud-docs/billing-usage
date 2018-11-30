---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-16"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Viewing your usage
{: #viewingusage}

You can view your usage details, including a summary of estimated charges for all resources, services, and support plans that are used per month in your organizations, from the Usage page in the {{site.data.keyword.Bluemix}} console.
{:shortdesc}

Billing managers can see the details for only the organizations in which they are assigned the Billing manager role. 
{: note}


## Viewing usage permissions
{: #view-usage-permissions}

For resources that are managed by Cloud Foundry, the Billing manager role must be applied at the org level. To see {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) resource usage, the Viewer role must be applied to the resource group. For more information about permission roles, see [IAM access](/docs/iam/users_roles.html#userroles), [Cloud foundry access](/docs/iam/cfaccess.html#cfaccess), or [Classic infrastructure permissions](/docs/iam/infrastructureaccess.html#infrapermission).

## Viewing service usage details 
{: #services}

In the services section, you can view a list of your services and the estimated costs that are associated with those services. To view a summary of estimated charges for all instances of a specific resource, complete the following steps: 

1. Go to **Manage > Billing and usage**, and select **Usage**. 
2. Click **View instances** to view all the instances of a specific type of resource.  
3. To see a detailed summary of estimated charges for each instance of a specific resource type, click **View instance details**. You can also see the detailed monthly usage metrics for the selected instance. 

The account owner is charged for the total usage that is incurred across all organizations at the end of each billing cycle. Each billing cycle lasts one month.

Account owners can filter the usage summary by group and select the time frame for usage. The charges that are shown represent the amount that you, as the account owner, are billed for that month.

If you select a specific organization from the **Filter by group** list, you can see the total usage for that organization, including any usage as part of a free tier. The free tier usage is shown as free at the account level, but not at the organizational level. When you view the organizational usage, you see the real usage for that organization, which includes both free and charged usage. All organizational usage is rolled up to the account usage after the free tier is removed.

The account manager of a Pay-As-You-Go account can set spending notifications against the total cost of the account, for runtime, services, and for individual services, excluding third-party services. For more information, see [Setting spending notifications](/docs/billing-usage/notifications.html).

## Exporting your usage details to a `.csv` file
{: #export-csv}

You can export a summary of your usage, or information about your services and instances, to a CSV file. By exporting your CSV file, you can easily find usage and cost information estimates for each resource for chargebacks to your customers or to understand more about your costs. 

1. Go to **Manage > Billing and usage**, and select **Usage**.
2. Click **Export CSV**.  


