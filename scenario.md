---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-30"

keywords: estimate cost, cost example, billing example, payment example, calculating app price

subcollection: billing-usage

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

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
| {{site.data.keyword.runtime_nodejs_short}}                   |	375 GB-hours free per month (shared across all runtimes)            |	$0.07 USD/GB-hour |
| {{site.data.keyword.autoscaling}} |	Free service plan for the {{site.data.keyword.autoscaling}} service |	Free              |
| {{site.data.keyword.cloudant_short_notm}} | Standard plan includes 20 GB of free data storage</br>Scale provisioned throughput capacity in increments of:</br>100 lookups per second</br>50 writes per second</br>5 queries per second | $1.00 USD/GB of data storage</br>$0.25 USD/Lookup per second</br>$0.50 USD/Write per second</br>$5.00 USD/Query per second |
{:caption="Table 1. Pricing for resources" caption-side="top"}


## Calculating the app price
{: #calc-app-price}

The price of the app can be calculated in the following way:

<dl>
<dt>Four 256-MB Node.js runtime instances</dt>
<dd>{{site.data.keyword.Bluemix_notm}} charges for a runtime by GB-hours. The number of GB used per month is <code>4 x 256 = 1024 MB or 1 GB per month</code>. Assume that there are <code>24 x 30 = 720 hours in a month</code>, so the application is charged for <code>1 x 720 = 720 GB-hours</code>.
<p>
375 GB-hours are included in a free allowance per month, which is shared across all {{site.data.keyword.Bluemix_notm}} runtimes. So the total cost for the runtime is <code>$0.07 x (720-375) = $24.15</code>.</p></dd>

<dt>Two {{site.data.keyword.autoscaling}} policies (processor and memory)</dt>
<dd>The {{site.data.keyword.autoscaling}} policies are free of charge.</dd>

<dt>150 GB per month {{site.data.keyword.cloudant_short_notm}}</dt>
<dd>The {{site.data.keyword.cloudant_short_notm}} for {{site.data.keyword.Bluemix_notm}} service charges are based on data storage and the ability to access that data by provisioned throughput capacity denoted by lookups, writes, and queries per second.
<p>
Add up the number of GB and deduct the 20-GB free allowance. 130 GB is charged per month. The total storage price includes the following parts:</p>
<pre class="codeblock">
<codeblock>
    130 x 1 = $130
    (1,000 / 100) x 0.25 = $2.50
    (500 / 50) x 0.50 = $5.00
    (50 / 5) x 5.00 = $50.00
</codeblock>
</pre>
<p>
The total price is 130 + 2.50 + 5.00 + 50.00 = $187.50.</p></dd>

<dt>20 GB inbound or outbound network traffic</dt>
<dd>Inbound and outbound network traffic is free of charge.</dd>

</dl>

When all the items are added, the total price of the application is $211.65.
