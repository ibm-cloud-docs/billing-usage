---

copyright:
  years: 2022, 2023
lastupdated: "2023-10-16"

keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, best practices

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}


# Best practices for lowering your account's carbon emissions
{: #account_setup}

These best practices help you to learn about {{site.data.keyword.cloud_notm}}'s carbon calculator features and options that you can use to track carbon emissions and reduce the carbon footprint of your account. To view your carbon emissions data, go to the [carbon calculator page](/billing/carbon-calculator). If you'd like to know more about the carbon calculator, see [Working with {{site.data.keyword.Bluemix_notm}}'s carbon calculator](/docs/billing-usage?topic=billing-usage-what-is-cloud-calc).


## Compress your data
{: #compress_data}

Compression is the conversion of data to a format that requires less storage space as measured in bits. This typically involves looking for patterns in data and eliminating redundancies. Audit video files, images, and archived files to determine if any can be compressed. Using less disc space means using less energy, which lowers emissions.


## Schedule jobs during off times
{: #low-usage-times}

Utilization reports are reviewed and updated monthly on the 15th of the month. This makes the final monthly data for the month available 7-10 days later in our system. If you do not need a month to day view, you should schedule your data pull for the last week of the month to have the final reviewed report for the month.

It is possible due to the high amount of users pulling data simultaneously, that the page load and refresh times may increase slightly during the last week of the month. If you do not need to have a month to date report, use the download option, this allows you to get the report data downloaded to your system. The report has all of the same data that is used to build the charts, but it is more efficient than gathering the information through the graphical interface.


## Leverage Envizi ESG reporting
{: #esg_reporting}

IBM Envizi is a robust data management foundation that is designed to create a single, trusted data source for all your ESG reporting and opportunity identification. Use ESG reporting to meet compliance and reporting requirements. For more information, see [IBM Envizi ESG Suite](https://www.ibm.com/products/envizi){: external}.

Envizi integration currently requires creation of a custom connector. Reach out to your {{site.data.keyword.cloud_notm}} representative for more information.

## Sunset underutilized components
{: #underutilized_components}

Cloud services have the characteristic that they are able to scale, if you find that you are no longer needing the additional capacity, it is a good practice to scale down the environments.

Lab environments might consume significant amounts of infrastructure and are generally under a specific subaccount. These environments should be temporary, and when they cease to be used, should be removed.

Some services are underutilized because they are deployed for every department. This might be needed to support compliance requirements (like data locality), but should be reviewed to identify in which cases they can be merged to increase the utilization, as this is more efficient than having additional environment deployments.
