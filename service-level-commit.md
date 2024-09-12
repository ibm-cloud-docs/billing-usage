---

copyright:
  years: 2024
lastupdated: "2024-09-11"

keywords: IBM Cloud billing, commitment model, using commitments, pay as you go with committed use, enterprise savings plan

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}


# Purchasing infrastructure services deployed on-premises
{: #service-comit}

Hybrid cloud services that can be deployed on-premises, like {{site.data.keyword.powerSysFull}} Private Cloud, often require a service-level commitment to order and deploy hardware at your site. With this commitment, you receive a discount on the standard metered rates for the service or bundle of services that you select.

Your on-premises usage data is sent to {{site.data.keyword.Bluemix_notm}} when your service-level commitment is activated, which allows you to monitor hardware usage alongside your cloud-based usage. Gain a complete view of your resource usage trends across both on-premises and cloud environments to help you make informed decisions.

Workloads that you deploy to your on-premises or edge environment are managed through {{site.data.keyword.satellitelong}}. For more information, see [Getting started with {{site.data.keyword.satellitelong}}](/docs/satellite?topic=satellite-getting-started).

Service-level commitments include a service or bundle of services, a term, discount rate, and total commitment amount. You might also have a monthly or yearly minimum spend if applicable. A term might be 6 months, 1 year, or 5 years. For example, you might have a commitment with the following provisions:
- 3-year term
- 30% discount on {{site.data.keyword.powerSys_notm}}
- $360,000 total commitment
- $1,000 minimum usage per month

All of your service usage in the bundle is discounted with a service-level commitment.

## Before you begin
{: #before-service-commit}



- The discount that you receive with a service-level commitment does not combine with other discounts, such as account-level discounts from an Enterprise Savings Plan or a Subscription. Your usage counts toward only one commitment at a time, and a service-level commitment supersedes an account-level discount.

## Signing up for a commitment
{: #signup-slc}

Most account types can order a service-level commitment. Work with [{{site.data.keyword.Bluemix_notm}} Cloud Sales](https://www.ibm.com/cloud?contactmodule){: external} to create a commitment quote based on you hardware needs and the spending amount for the period that you want to commit to.

You can have multiple commitments for different services active at the same time.
{: note}

After you accept the commitment quote, you receive an email to confirm that your payment information is processed and that the commitment is added to your account. When the contract term ends, service commitments are automatically converted to Pay-As-You-Go and you're charged on-demand pricing for those services.


### Ordering managed hardware
{: #ordering-slc}

Managed hardware is physical hardware like servers, storage, and networking equipment, which {{site.data.keyword.IBM_notm}} provides and maintains based on the capacity and performance requirements in your order. To order your on-premises private cloud service, discuss your requirements with [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} or your IBM Business Partner.

After you agree to the commitment terms and sign the commitment contract, your hardware order is placed. Your commitment start date begins after the hardware is delivered and set up in your data center. When the hardware is deployed, the commitment is active and you can begin monitoring your hardware usage, service charges, and any additional costs within the {{site.data.keyword.Bluemix_notm}} console.

## Viewing your commitment usage
{: #slc-services}

To view your service-level commitment usage, go to **Manage > Billing and usage > Commitments** and click **Service-level commitments**. To access this information, you need an access policy with the viewer role or higher on the billing account management service.

### Tracking usage for service-level commitments
{: #slcu-usage-2}

Download your usage report by [Exporting your account usage details to a CSV file](/docs/billing-usage?topic=billing-usage-viewingusage&interface=ui#export-csv) or [Exporting your enterprise usage details to a .csv file](/docs/billing-usage?topic=billing-usage-enterprise-usage&interface=ui#export-enterprise-csv).

{{site.data.content.on-prem-commit}}

{{site.data.content.enterprise-commit}}

## Minimum spending
{: #spending-min-slc}

Multi-year terms have a required yearly minimum spend. You might also have a monthly minimum spend for a commitment, which depends on your commitment amount. If you don't meet the monthly or yearly minimum usage, you are charged up to the minimum remaining amount. To make sure that you're using resources at a rate that fulfills your commitment, go to the Service-level commitments page and click a commitment. Here you can view a more detailed breakdown of your usage.

Set a spending notification to make sure that your usage is on track to fulfill your commitment. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).
{: tip}

## Getting support
{: #support-slc}

You can get Advanced or Premium support with your service-level commitment. The level of support that you select determines the severity that you can assign to support cases and your level of access to the tools available in the Support Center. To get support, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external}.

For more information about {{site.data.keyword.Bluemix_notm}} support plans, see [Basic, Advanced, and Premium Support plans](/docs/get-support?topic=get-support-support-plans).
