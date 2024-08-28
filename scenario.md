---

copyright:
  years: 2015, 2024
lastupdated: "2024-08-28"

keywords: estimate cost, cost example, billing example, payment example, calculating app price

subcollection: billing-usage

---

{{site.data.keyword.attribute-definition-list}}



# Scenario: Estimating costs of an example Node app
{: #sample}

Assume that you have a Node.js web app with scaling capabilities, and the app uses several services that are provided by {{site.data.keyword.Bluemix}}. You can learn how the actual cost of your app is calculated in this example.
{: shortdesc}

The web app uses the following {{site.data.keyword.Bluemix_notm}} services and items:

* Four 256-MB Node.js runtime instances
* Two {{site.data.keyword.autoscaling}} policies, processor and memory
* 150 GB per month {{site.data.keyword.cloudant_short_notm}} database, 1,000 lookups, 500 writes, and 50 queries
* 20 GB inbound or outbound network traffic


## Prices for {{site.data.keyword.Bluemix_notm}} resources
{: #sample_resources}

To keep the example simple, assume the prices in the following table don't fluctuate within or between a time frame, for example, a month. All pricing in this example is in US currency.

| Service                           |	Features                                                            |	Price             |
|-----------------------------------|---------------------------------------------------------------------|-------------------|
| {{site.data.keyword.runtime_nodejs_short}}                   |	Charges for runtime by GB-hours          |	$0.07 USD/GB-hour |
| {{site.data.keyword.autoscaling}} |	Free service plan for the {{site.data.keyword.autoscaling}} service |	Free              |
| {{site.data.keyword.cloudant_short_notm}} | The standard plan includes 20 GB of data storage at no cost  \n Scale provisioned throughput capacity in increments of:  \n 100 lookups per second  \n 50 writes per second  \n 5 queries per second | $1.00 USD/GB of data storage  \n $0.25 USD/Lookup per second  \n $0.50 USD/Write per second  \n $5.00 USD/Query per second |
{: caption="Table 1. Pricing for resources" caption-side="top"}


## Calculating the app price
{: #calc-app-price}

The price of the app can be calculated in the following way:

Four 256-MB Node.js runtime instances
:   {{site.data.keyword.Bluemix_notm}} charges for a runtime by GB-hours. The number of GB used per month is `4 x 256 = 1024 MB` or 1 GB per month. Assume that there are `24 x 30 = 720` hours in a month, so the application is charged for `1 x 720 = 720` GB-hours.

Two {{site.data.keyword.autoscaling}} policies (processor and memory)
:   The {{site.data.keyword.autoscaling}} policies are without charge.

150 GB per month {{site.data.keyword.cloudant_short_notm}}
:   The {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} service charges are based on data storage and the ability to access that data by provisioned throughput capacity denoted by lookups, writes, and queries per second.

   Add up the number of GB and deduct the 20-GB that is without charge. 130 GB is charged per month. The total storage price includes the following parts:

   ```screen
   130 x 1 = $130
   (1,000 / 100) x 0.25 = $2.50
   (500 / 50) x 0.50 = $5.00
   (50 / 5) x 5.00 = $50.00
   ```

   The total price is 130 + 2.50 + 5.00 + 50.00 = $187.50.

20 GB inbound or outbound network traffic
:   Inbound and outbound network traffic is without charge.


When all the items are added, the total price of the application is $211.65.
