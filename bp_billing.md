---

copyright:
  years: 2019
lastupdated: "2019-06-20"

keywords: best practice billing, best practice usage, automate billing, track costs

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Best practices for billing and usage
{: #best-practices}

Follow our best practices to track costs and automate billing in {{site.data.keyword.Bluemix}}.
{:shortdesc}


## Track costs for related resources by adding tags
{:#track-billing-tags}

Add tags to your resources to organize, track, and manage costs for related resources. When you use a consistent tagging schema to identify which resources are tied to specific projects, you can group and filter by those tags when you analyze costs within your exported usage report.

1. Tag your resources by using a consistent tagging schema, such as creating tags to differentiate cost centers, data centers, projects, or teams. To add tags, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list**. In the Tag column, click **Add tag** for each resource that you want to tag.

   Add tags in key:value pairs to add custom columns based on the key in the usage report. Create keys based on the categories that you use to organize your resources, such as using `costcenter:` to group by cost center or `project:` to group by project.
   {: tip}

   For example, you might have resources for two projects in a single account, Project ABC and Project XYZ. Project ABC has a {{site.data.keyword.containershort_notm}} cluster, a few Cloud Foundry app deployments, and an {{site.data.keyword.cloudant_short_notm}} database. You can add the `project:abc` tag to all of these resources to distinguish these resources for Project ABC from similar resources in Project XYZ that are tagged `project:xyz`.

   For more information about adding and using tags, see [Working with tags](/docs/resources?topic=resources-tag).

1. Track costs for the tagged resources by exporting the usage report for your instances. To export the report, go to **Manage > Billing and usage**, and select **Usage**. Then, click **Export CSV > Instance**.

   Use the Tags column in the instance CSV file to help analyze the resources in your account. You can sort the CSV data according to the project tag on each instance so that you can better analyze the individual projects' cost. If you tagged your resources with key:value pairs, you'll also see columns in the usage report that correspond with the key. For example, resources tagged `project:abc` and `project:xyz` appear in a Project column as `abc` and `xyz`.

   For more information, see [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## Automate billing and usage management by using the CLI or APIs
{: #billing-cli-apis}

If you want to automate how you review your resource usage and any associated costs, you can use the [`ibmcloud billing`](/docs/cli?topic=cloud-cli-ibmcloud_billing) CLI or the [Usage Metering ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/usage-metering){: new_window} and [Usage Reports ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/apidocs/metering-reporting){: new_window} APIs to integrate this functionality into your own apps.

To get started using the APIs, set up the [{{site.data.keyword.Bluemix_notm}} usage sample dashboard ![External link icon](../icons/launch-glyph.svg)](https://github.com/IBM-Cloud/openwhisk-cloud-usage-sample){: new_window}. Using {{site.data.keyword.openwhisk}}, the sample implements an API-driven approach to obtain and visualize {{site.data.keyword.Bluemix_notm}} usage and billing data.
{: tip}
