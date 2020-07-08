---

copyright:
  years: 2019, 2020
lastupdated: "2020-05-27"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:external: target="_blank" .external}


# Best practices for billing and usage
{: #best-practices}

Follow our best practices to track costs and automate billing in {{site.data.keyword.Bluemix}}.
{:shortdesc}

## Choose an account type that fits your usage
{: #choose-account-types}

{{site.data.keyword.cloud_notm}} has two billable account types, Pay-As-You-Go and Subscription accounts. Being billable means that if you have these account types, you can use {{site.data.keyword.cloud_notm}} resources and services that cost money. The account type that you choose impacts how you're billed for your resource usage.
* With Pay-As-You-Go accounts, you're billed monthly for your resource usage. You pay only for what you use, with no long-term contracts. As your resource usage fluctuates, so does your invoice, similar to a utility bill. This account type is a good fit for developers or companies that want to explore the entire {{site.data.keyword.cloud_notm}} catalog but have smaller or variable workloads.
* With Subscription accounts, you buy a subscription for an amount of credit to spend on resource usage within a certain time period. In exchange for this spending commitment, you get a discount on your usage costs. For example, you might buy a subscription for $12,000 a year that comes with a 10% discount. No matter when you incur usage costs within the year, you get fixed billing for the subscription amount, such as $1,000 a month. This account type is ideal for enterprise organizations with large cloud workloads that want the predictability of fixed billing for their financial planning. For more information about how subscriptions work, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions).

Each of these account types includes more benefits for your production workloads on {{site.data.keyword.cloud_notm}}, including access to the entire catalog, extra free runtime memory, and support plans. For more information, see [Account types](/docs/account?topic=account-accounts).

## Track costs for related resources by adding tags
{:#track-billing-tags}

Add tags to your resources to organize, track, and manage costs for related resources. When you use a consistent tagging schema to identify which resources are tied to specific projects, you can group and filter by those tags when you analyze costs within your exported usage report.

1. Tag your resources by using a consistent tagging schema, such as creating tags to differentiate cost centers, data centers, projects, or teams. To add tags, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list**. In the Tag column, click **Add tag** for each resource that you want to tag.

   Add tags in key:value pairs to add custom columns based on the key in the usage report. Create keys based on the categories that you use to organize your resources, such as using `costcenter:` to group by cost center or `project:` to group by project.
   {: tip}

   For example, you might have resources for two projects in a single account, Project ABC and Project XYZ. Project ABC has a {{site.data.keyword.containershort_notm}} cluster, a few Cloud Foundry app deployments, and an {{site.data.keyword.cloudant_short_notm}} database. You can add the `project:abc` tag to all of these resources to distinguish these resources for Project ABC from similar resources in Project XYZ that are tagged `project:xyz`.

   For more information about adding and using tags, see [Working with tags](/docs/resources?topic=resources-tag).

1. Track costs for the tagged resources by exporting the usage report for your instances. To export the report in the IBM Cloud console, go to **Manage > Billing and usage**, and select **Usage**. Then, click **Export CSV > Instance**.

   Use the Tags column in the instance CSV file to help analyze the resources in your account. You can sort the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. If you tagged your resources with key:value pairs, you'll also see columns in the usage report that correspond with the key. For example, resources tagged `project:abc` and `project:xyz` appear in a Project column as `abc` and `xyz`.

   For more information, see [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automate billing and usage management by using the CLI or APIs
{: #billing-cli-apis}

If you want to automate how you review your resource usage and any associated costs, you can use the [`ibmcloud billing`](/docs/cli?topic=cli-ibmcloud_billing#ibmcloud_billing_org_usage) CLI or the [Usage Metering ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: external} and [Usage Reports ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: external} APIs to integrate this functionality into your own apps.

To get started using the APIs, set up the [{{site.data.keyword.Bluemix_notm}} usage sample dashboard ![External link icon](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: external}. Using {{site.data.keyword.openwhisk}}, the sample implements an API-driven approach to obtain and visualize {{site.data.keyword.Bluemix_notm}} usage and billing data.
{: tip}
